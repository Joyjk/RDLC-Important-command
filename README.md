#RDLC Importent commands
1. If data set return null then hide row of table--------------------->  =Fields!Vleugel.Value Is Nothing
2. If data set return null then show another value ------------------->  =iif(Fields!ABC.Value Is Nothing, "value is NULL", "value is not NULL") 
3. If Data contains Specific string then show another value ---------->  =iif(Fields!admission_no.Value.ToString().Contains("ER"),"TRUE","Falsee")
4. Row Visibility Show or Hide Based on condition --------------------> =IIF(Fields!service_name.Value="Consultancy",TRUE,FALSE)
5. Row Visibility show or hide based on condition ---------------------> =IIF(((Fields!service_name.Value="Consultancy") AND (Fields!charge.Value<0)) , TRUE,FALSE)



#RDLC sum
=iif((Sum(Fields!total_amount.Value, "ds") + Sum(Fields!charge.Value, "ds4")) -Sum(Fields!paid_amount.Value, "ds3"),0,(Sum(Fields!total_amount.Value, "ds") + Sum(Fields!charge.Value, "ds4")) -Sum(Fields!paid_amount.Value, "ds3"))
