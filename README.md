# awsbilltilldate
A single command to output your AWS monthly bill till date.


Just run this command. if you have run aws configure already, the command should simply output the value in USD


#aws ce get-cost-and-usage --time-period Start=`date +"%Y-%m-01"`,End=`date +"%Y-%m-%d"` --granularity MONTHLY --metrics "BlendedCost" | awk '{print $2}' | tail -1
