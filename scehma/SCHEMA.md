# Databse Schema for VIDPORT (Open Source Video Sharing Platform)

- ### User Data Schema 
    

    - #### USER Login Information
        ```sql
            user_credentials : {
                    sl_no [INT(100)] AUTO_INCREMENT_BY_ID PRIMARY_KEY(),
                    user_id [VARCHAR(15)],
                    password [VARCHAR(50)]
                }
        ```
    <br/>

    - #### USER Personal Information
        ```sql
            user_info : {
                sl_no [INT(100)] AUTO_INCREMENT_BY_ID PRIMARY_KEY(),
                user_id [VARCHAR(15)],
                first_name [VARCHAR(20)],
                middle_name [VARCHAR(20)],
                last_name [VARCHAR(20)],
                age [VARCHAR(3)]
                email [VARCHAR(30)],
                phone_no [VARCHAR(25)]
            },

            user_address : {
                sl_no [INT(100)] AUTO_INCREMENT_BY_ID PRIMARY_KEY(),
                user_id [VARCHAR(15)],
                country [VARCHAR(35)],
                state [VARCHAR(35)],
                address_line_one [VARCHAR(200)],
                address_line_two [VARCHAR(200)],
                pincode [VARCHAR(6)]
            }
        ```
    <br/>

    - #### USER Account Information
        ```sql
            user_account : {
                sl_no [INT(100)] AUTO_INCREMENT_BY_ID PRIMARY_KEY(),
                user_id [VARCHAR(15)],
                handle [VARCHAR(25)],
                handle_locked [BOOLEAN],
                email_verified [BOOLEAN],
                phone_no_verified [BOOLEAN],
                profile_id [VARCHAR(40)],
                timestamp [TIMESTAMP],
                ip [VARBINARY(16)],
                account_active [BOOLEAN]
            }
        ```
    <br/>

    - #### USER Profile Information

        ```sql

            user_profile : {
                sl_no [INT(100)] AUTO_INCREMENT_BY_ID PRIMARY_KEY(),
                profile_id [VARCHAR(40)],
                profile_picture [VARCHAR(25)],
                visble_name [VARCHAR(30)]
            },

            user_profile_tweaks : {
                sl_no [INT(100)] AUTO_INCREMENT_BY_ID PRIMARY_KEY(),
                profile_id [VARCHAR(40)],
                show_email_id [BOOLEAN] {0},
                show_phone_no [BOOLEAN] {0},
                theme [INT(10)],
            }
        ```
    
    - ### USER Content Creator Information

        ** **This Section is yet to be created** **