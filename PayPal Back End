def importCreditCardInfo():
    card_info = []
    card_info_block = []


    loadManager = open('creditCardInfo.txt', 'r')
    data_dump = loadManager.read()


    equa_counter = 0
    sep_counter = 0


    print(data_dump)


    for c_site in range(len(data_dump)):
        if(data_dump[c_site] == '/'):
            splice_start = c_site + 1
            splice_end = splice_start
                
            while ((data_dump[splice_end] != '/') and (data_dump[splice_end] != '=') and (data_dump[splice_end] != '_')):
                splice_end += 1
            
            segment = data_dump[splice_start:splice_end]


            card_info.append(segment)


        if(data_dump[c_site] == '_'):
            card_info_block.append(card_info[:])
            card_info = []             


        
    loadManager.close()
    return card_info_block


print(importCreditCardInfo())


def VerifyUser(user_info,username_input,password_input):
    
    for val in user_info:
        user_one = user_info[0]
        user_two = user_info[1]
        
        for user_name in user_one:
            if username_input == user_one[0]:
                if password_input == user_one[1]:
                        print('True')
                        break
        for user_name in user_two:
            if username_input == user_two[0]:
                if password_input == user_two[1]:
                    print('True')
                    break
        break








username_input = input('Enter Username :')
password_input = input('Enter Password :')
user_info = [['mking2016', 'hackath0n', 'Matthew King', '1234567887654321', '500'], ['jwalk2016', 'walking', 'Jessica Walker', '8765432112345678', '550']]
VerifyUser(user_info,username_input, password_input)
