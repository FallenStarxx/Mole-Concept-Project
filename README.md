#Made in Python 3.5.2
###################
#Computing Project#
###################

result=0

def type1moleCAL(x):
    return x*(6.00*(10**23))

def type1partCAL(x):
    return x/(6.00*(10**23))

def type2massCAL():
    return molarmass*moles

def type2molarmassCAL():
    return mass/moles

def type2moleCAL():
    return mass/molarmass

def type3gasCAL():
    return final_input*24

def type3moleCAL():
    return final_input/24

choice=int(input('Please select a function:\n1.Content Information\n2.Calculator\n3.Quiz\n'))

if choice==1: 
    print('Go to: http://gg.gg/MoleConcept')

elif choice==2: 
    type_cal=int(input('Please select the formula which you wish to use:\n1.Moles=Particles/Avogadros Constant\n2.Moles=Mass/Molar Mass\n3.Moles=Volume of Gas/24\n'))

    if type_cal==1: #Moles=Particles/Avogadros Constant Calculator#
        input_type=int(input('Please indicate what type of input you are inputing:\n1.Moles\n2.Particles\n'))
        final_input=float(input('Please input a number:'))

        if input_type==1: #Molecule Calculation#
            result= type1moleCAL(final_input)
            print('Number of molecules=',result)

        elif input_type==2: #Moles Calculation#
            result= type1partCAL(final_input)
            print('Number of moles=',result)

    elif type_cal==2: #Moles=Mass/Molar Mass Calculator#
        input_type=int(input('Please indicate what are you calculating:\n1.Mass\n2.Molar Mass\n3.Moles\n'))

        if input_type==1: #Mass Calculator#
            molarmass=int(input('Please input Molar Mass:'))
            moles=float(input('Please input number of Moles:'))
            print('Mass=',type2massCAL())

        elif input_type==2: #Molar Mass Calculator#
            mass=float(input('Please input Mass:'))
            moles=float(input('Please input number of Moles:'))
            print('Molar Mass=',type2molarmassCAL())

        elif input_type==3: #Mole Calculator#
            mass=float(input('Please input Mass:'))
            molarmass=int(input('Please input Molar Mass:'))
            print('Number of Moles=',type2moleCAL())

    elif type_cal==3: #Moles=Volume of Gas/24#
        input_type=int(input('Please indicate what type of input you are inputing:\n1.Moles\n2.Volume of Gas\n'))

        if input_type==1: #Volume of Gas Calculator#
            final_input=float(input('Please input number of Moles:'))
            print('Volume of Gas=',type3gasCAL())

        elif input_type==2: #Mole Calculator#
            final_input=float(input('Please input Volume of Gas in dm3:'))
            print('Number of Moles=',type3moleCAL())

elif choice==3: 
    diff=int(input('Select Quiz Difficulty:\n1.Novice\n2.Intermediate\n3.Advanced\n'))
    if diff==1: 
                  
        question1=int(input('Question 1: How many moles are there in 2.35 x 10**23 neon atoms?\n1.0.432\n2.0.392\n3.0.391\n'))
        if question1==2:
            result+=1
            print('Correct!')
        else:
            print('Incorrect!')
                  
        question2=int(input('Question 2: How many moles are there in 1.82 x 10**24 carbon dioxide molecules?\n1.3.54\n2.2.34\n3.3.07\n'))
        if question2==3:
            result+=1
            print('Correct!')
        else:
            print('Incorrect!')
                  
        question3=int(input('Question 3: How many molecules are there in 0.325 moles of ammonia gas?\n1.1.95e+23\n2.1.45e+23\n3.2.05e+24\n'))
        if question3==1:
            result+=1
            print('Correct!')
        else:
            print('Incorrect!')
                  
        question4=int(input('Question 4: How many molecules are there in 0.692 moles of lead(II) iodide?\n1.4.15e+23\n2.2.14e+24\n3.3.95e+23'))
        if question4==1:
            result+=1
            print('Correct!')
        else:
            print('Incorrect!')
                  
        question5=int(input('Question 5: How many molecules are there in 1.76 moles of iron(III) nitride?\n1.1.34e+24\n2.2.15e+24\n3.1.06e+24'))
        if question5==3:
            result+=1
            print('Correct!')
        else:
            print('Incorrect!')
                  
        if result==0:
            print('You scored',str(result)+'/5. Revise your formulas!')
        if result==1 or result==2:
            print('You scored',str(result)+'/5. Try harder!')
        if result==3:
            print('You scored',str(result)+'/5. You can do better!')
        if result==4 or result==5:
            print('You scored',str(result)+'/5. Well done!')
                  
    elif  diff==2: #Intermediate Difficulty#
                  
        question1=input('Question 1: What is the volume of 1.50 moles of nitrogen, N2?(Indicate units here as dm3)')
        if question1=='36.0dm3':
            result+=1
            print('Correct!')
        else:
            print('Incorrect!')
                  
        question2=input('Question 2: What is the number of moles in 600cm3 of hydrogen?(Inidcate units)')
        if question2=='0.0250mol':
            result+=1
            print('Correct!')
        else:
            print('Incorrect!')

        question3=input('Question 3: What is the mass of 155cm3 of carbon dioxide?(Indicate units)')
        if question3=='0.284g':
            result+=1
            print('Correct!')
        else:
            print('Incorrect!')

        question4=input('Question 4: Calculate the relative molecular mass of 1200cm3 of gas which weighs 3.20g.')
        if question4=='64.0':
            result+=1
            print('Correct!')
        else:
            print('Incorrect!')
            
        question5=input('Question 5: Calculate the relative molecular mass of 6dm3 of gas which weighs 17.8g.')
        if question5=='71.2':
            result+=1
            print('Correct!')
        else:
            print('Incorrect!')

        if result==0:
            print('You scored',str(result)+'/5. Revise your formulas!')
        if result==1 or result==2:
            print('You scored',str(result)+'/5. Try harder!')
        if result==3:
            print('You scored',str(result)+'/5. You can do better!')
        if result==4 or result==5:
            print('You scored',str(result)+'/5. Well done!')
            
    elif diff==3: #Advanced Difficulty#
        
        question1=input('Question 1: Calculate the number of atoms for 0.745 moles of chlorine.')
        if question1=='8.94e+23':
            result+=1
            print('Correct!')
        else:
            print('Incorrect!')

        question2=input('Question 2: Calculate the number of molecules for 12g of hydrogen, H2.')
        if question2=='3.60e+24':
            result+=1
            print('Correct!')
        else:
            print('Incorrect!')

        question3=input('Question 3: Calculate the mass of 12e+23 nitrogen, N2 molecules.(Indicate units as dm3 here)')
        if question3=='48.0dm3':
            result+=1
            print('Correct!')
        else:
            print('Incorrect!')
    
        question4=input('Question 4: What is the empirical formula of a compound of 80% copper and 20% sulfur?')
        if question4=='Cu2S':
            result+=1
            print('Correct!')
        else:
            print('Incorrect!')

        question5=input('Question 5: The empirical formula of glucose is CH2). Its relative molecular mass is 180. Find the molecular formula.')
        if question5=='C6H1206':
            result+=1
            print('Correct!')
        else:
            print('Incorrect!')

        if result==0:
            print('You scored',str(result)+'/5. Revise your formulas!')
        if result==1 or result==2:
            print('You scored',str(result)+'/5. Try harder!')
        if result==3:
            print('You scored',str(result)+'/5. You can do better!')
        if result==4 or result==5:
            print('You scored',str(result)+'/5. Well done!')
