# MFIS Bank Decision Support System
 A decision-support system for granting personal loans using Mamdanis fuzzy inference system.
The decision whether or not to grant the loan is based on the following information about the applicant and the application:
• Income level.
• Assets in possession: real estate, vehicles, etc.
• Employment stability: seniority, type of contract, etc.
• Loan amount in relation to monthly income.
• Loan and payment history.
• Age.
Each of these variables is typified by one or more fuzzy sets whose membership functions have trapezoidal or triangular shapes, that is, they are composed of straight segments. The file InputVarSets.txt contains the description of these sets, one set in each line. The format is:
var = label , xmin , xmax , a, b, c, d
Where
• var corresponds to one of the input variables (“age”, “income”, ...)
• label is the name of the fuzzy set in question (“young”, “adult”, ...)
• xmin , xmax determine the range of
values of var
• a, b, c, d are the significant points of
the trapezoid, as shown in this example:
The result of the inference system will be the
risk level of the request.
Several bank experts have provided the rules found in Rules.txt . The format of each rule is name, var0 =label0 , var1 =label1 , ... varn = labeln
Where:
• name is the name of the rule
• var0 =label0 is the consequent of the rule
• var1 =label1 AND ... AND varn = labeln is the antecedent of the rule
The antecedent of the rules only supports the logical AND operator. In the file it appears as a list of var = label pairs , but the AND is implicit.
