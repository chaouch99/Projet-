# Projet-

#SERIE1_EX1

import numpy as np
data = np.loadtxt('ECGu.txt')
ecg1=(data[:,0])/1000
ecg2=(data[:,1])/1000
ecg3=(data[:,2])/1000
# frequency is 
frequency = 1024
  
# calculating time data with ecg size along with frequency
time_data = np.arange(ecg1.size) / frequency
time_data2 = np.arange(ecg2.size) / frequency
time_data3 = np.arange(ecg3.size) / frequency

# plotting time and ecg model
plt.plot(time_data, ecg1)

plt.plot(time_data2, ecg2)

plt.plot(time_data3, ecg3)

plt.xlabel("time in seconds")
plt.ylabel("ECG in milli Volts")

plt.xlim(0, 7) 
plt.ylim(-0.5, 0.8)

# display
plt.show()
