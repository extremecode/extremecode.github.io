keytool -genkey -keyalg RSA -keystore server.keystore -storepass secret -keypass secret -validity 365  -dname "cn=Server Administrator,o=DE,c=DE"

keytool -importkeystore -srckeystore server.keystore -destkeystore server.keystore -deststoretype pkcs12

keytool -genkey -keystore client.keystore -storepass secret -validity 365 -keyalg RSA -keysize 2048 -storetype pkcs12 -dname "cn=Desktop user,o=DE,c=DE"

keytool -importkeystore -srckeystore client.keystore -destkeystore client.keystore -deststoretype pkcs12

keytool -exportcert -keystore client.keystore  -storetype pkcs12 -storepass secret -keypass secret -file client.crt

keytool -importkeystore -srckeystore client.keystore -srcstorepass secret -destkeystore clientCert.p12 -srcstoretype PKCS12 -deststoretype PKCS12 -deststorepass secret
