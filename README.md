#RDLC Importent commands
1. If data set return null then hide row of table--------------------->  =Fields!Vleugel.Value Is Nothing
2. If data set return null then show another value ------------------->  =iif(Fields!ABC.Value Is Nothing, "value is NULL", "value is not NULL") 
3. If Data contains Specific string then show another value ---------->  =iif(Fields!admission_no.Value.ToString().Contains("ER"),"TRUE","Falsee")
