# datasciencecoursera

PC<- read.csv("C:/Users/MartinFelipe/SkyDrive/household_power_consumption.txt", sep=";",
colClasses=c("character", "character", rep("numeric",7)),na="?") 
subset<- PC[PC$Date %in% c("1/2/2007","2/2/2007") ,]
png("plot1.png", width=480, height=480)
hist(subset$Global_active_power, col="red", main="Global Active Power", xlab="Global Active Power (kilowatts)")
dev.off()

