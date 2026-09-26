### userdetails--Part 2
echo "username: admin password: P@ssw0rd123 Email: admin@example.com Phone : 123-456-7890" > userdetails

openssl rand -hex 32
openssl rand -hex 32 > passkey && cat passkey

Step 3
openssl enc -aes-256-cbc -salt -pbkdf2 -in userdetails -out userdetails_encrypt -pass file:passkey


step 4
 cat userdetails_encrypt

 Step. 5

 openssl enc -aes-256-cbc -d -pbkdf2 -in userdetails_encrypt -out userdetails_decrypt -pass file:passkey

 Step 5

 userdetails_decrypt
