in this part, we’re going to deploy two applications “mongoDB” & “mongo-express”

I.      create a Mongodb Deployment, wich have its Pod.
II.     create a Secret that contains (DB_User & DB_Pwd). MongoDB Pod of MongoDB Deployment will need credentials to authenticatd to the DB.
III.    create a MongoDB Internal Service to communicate the pod with other component in the same cluster
IV.     create a Mongo Express Deployment, wich had its Pod (it will communicate with the MongoDB using the Internal Service)
V.      create a ConfigMap that contains (database_url), because Mongo Express Pod of Mongo Express Deployment will need database url.
VI.     create a Mongo Express External Service to be acces from browser