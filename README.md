# NYC-Cab-Data-Analysis-Google-Cloud-Platform

## The goal of this project is to determine the mean and the variance of the trip cost for trips originating in each taxi zone
1. The PULocationID column corresponds to the taxi zone
2. The trip cost is the fare_amount plus the tip_amount.
3. Used combineByKey and the one pass method for calculating both the mean as well as the variance. 
4. Used the following formula for calculating variance:  𝑣𝑎𝑟𝑖𝑎𝑛𝑐𝑒=∑𝑥2𝑖−𝑛𝑥¯2(𝑛−1) 
5. The program should output a Map of (zone -> (mean,variance), zone -> (mean,variance) , ......
6. Example of output:

Map(188 -> (14.666259597276545,249.33821353365235), 204 -> (55.0072972972973,2666.6166251278305), 194 -> (42.80580259365995,915.6050500618951), ....


### Steps to run the Google Cloud Platform
1. Choose Compute engine from the navigation menu on google cloud console
2. Launch an ssh shell (the first option on the SSH dropdown menu at the end of the VM entry)
3. Click on the gear icon on the top right corner of the shell window
4. Choose upload file and upload the shell script. The script will now be in the home directory of your virtual machine (note that this is not your storage bucket!)
type chmod u+x get_files.sh to make the script executable
5. Create the taxi directory using the command mkdir /cloud-console-2020/taxi (replace cloud-console-2020 with the name of your own storage bucket)
6. Run get_files.sh with the command ./get_files.sh
7. This will take a while but curl will give you download stats as it downloads each file
8. Once completed, navigate to your storage bucket on google cloud console and make sure the files are in the bucket
