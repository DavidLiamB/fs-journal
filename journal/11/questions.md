# A bit more CSharp and SQL
1. What does ***inheritance*** accomplish for us in C#?

  > | allows the child or the inheritance to get all of it parents accessibly members |

2. How does ***member inheritance*** work in C#? Does a `Class` inherit all members of the base `Class`?

  > | member inheritance in c# works by passing down the members of the patient class down to the child class. not all member are inherited only the accessibly one like public and not the private one and protected one can only be seen |

3. How does ***accessibility*** affect inheritance?

  > | cant inherit from or thing that are private or inaccessibly |

4. What is the difference between a `PRIMARY KEY` and a `FOREIGN KEY`

  > | a primary key is a unique property for the object on the table so i can identify while the foreign key is the primary key to a different object |

5. What is an ***alias***?

  > | a alterative name for a table that you assign to it to make referring to the table easier |

6. Demonstrate how you would query a join statement that would get all of a doctors patients from the following collections:

  ```SQL
  CREATE TABLE doctors (
    id INT NOT NULL AUTO_INCREMENT,
    -- CODE OMITTED
    PRIMARY KEY (id)
  )

  CREATE TABLE patients (
    id INT NOT NULL AUTO_INCREMENT,
    -- CODE OMITTED
    PRIMARY KEY (id)
  )

  CREATE TABLE patient_doctors (
    id INT NOT NULL AUTO_INCREMENT,
    doctorId INT NOT NULL,
    patientId INT NOT NULL,

    FOREIGN KEY (doctorId)
      REFERENCES doctors(id),
    FOREIGN KEY (patientId)
      REFERENCES patients(id),
  )

  ```

  > | 
  string sql = @"
  SELECT
  doc.*,
  pat.*
  FROM patient_doctors doc
    JOIN patients pat ON pat.Id = doc.patientId
  WHERE doc.Id = @patientDoctorId;";

  _db.Query<PatientDoctor, DoctorsPatient, DoctorsPatient>(sql, ()=>{
    DoctorsPatient.PatientDoctorId = PatientDoctor.Id;
    DoctorsPatient.DoctorId = PatientDoctor.DoctorId;
    return DoctorsPatient;
  }, new {patientDoctorId}).FirstOrDefault(); 
  
  
  |
