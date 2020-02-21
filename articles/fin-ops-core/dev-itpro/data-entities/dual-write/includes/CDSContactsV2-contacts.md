## <a name="cds-contacts-v2-to-contacts"></a>CDS-i kontakti V2 kontaktidele

See mall sünkroonib andmeid rakenduste Finance and Operations ja Common Data Service'i vahel.

Allika filter: (AssociatedContactType = 1)

Ümber pööratud allika filter: msdyn_contactforvendor eq true ja msdyn_sellable eq false ja msdyn_contactpersonid ne ''

Finance and Operationsi väli | Kaardi tüüp | Muu Dynamics 365 väli | Vaikeväärtus
---|---|---|---
CONTACTPERSONPARTYNUMBER | = | msdyn_partynumber | 
ASSOCIATEDCONTACTTYPE | << | puudub | Hankija
FIRSTNAME | = | firstname | 
MIDDLENAME | = | middlename | 
LASTNAME | = | lastname | 
ASSOCIATEDCONTACTNUMBER | = | msdyn_vendorcontactid.msdyn_vendoraccountnumber | 
PRIMARYADDRESSCITY | = | address1_city | 
PRIMARYADDRESSCOUNTRYREGIONID | = | address1_country | 
PRIMARYADDRESSCOUNTYID | = | address1_county | 
PRIMARYFAXNUMBER | = | faks | 
PRIMARYADDRESSSTATEID | = | address1_stateorprovince | 
PRIMARYADDRESSSTREET | = | address1_line1 | 
PRIMARYADDRESSZIPCODE | = | address1_postalcode | 
PRIMARYPHONENUMBER | = | telephone1 | 
PRIMARYEMAILADDRESS | = | emailaddress1 | 
EMPLOYMENTDEPARTMENT | = | osakond | 
MÄRKUSED | = | kirjeldus | 
SUGU | >< | gendercode | 
GOVERNMENTIDENTIFICATIONNUMBER | = | governmentid | 
PRIMARYURL | = | websiteurl | 
MARITALSTATUS | >< | familystatuscode | 
ISRECEIVINGDIRECTMAIL | >< | donotemail | 
EMPLOYMENTPROFESSION | = | jobtitle | 
SPOUSENAME | = | spousesname | 
puudub | >> | msdyn_contactforvendor | Tõene
CONTACTPERSONID | = | msdyn_contactpersonid | 
