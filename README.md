import pandas as pd
import matplotlib.pyplot as plt

sports_data = {
    'Name': ['LeBron James', 'Cristiano Ronaldo', 'Lionel Messi', 'Usain Bolt', 'Serena Williams', 'Tom Brady'],
    'Income_Million': [96, 117, 126, 34, 29, 76],
    'Age': [37, 36, 34, 35, 40, 44],
    'Sport': ['Basketball', 'Football', 'Football', 'Track and Field', 'Tennis', 'American Football']
}

sports_billionaires_data = pd.DataFrame(sports_data)

correlation_coefficient_sports= sports_billionaires_data['Age'].corr(sports_billionaires_data['Income_Million'])

plt.scatter(sports_billionaires_data['Age'], sports_billionaires_data['Income_Million'])
plt.title('Age vs Income\nCorrelation Coefficient: {:.2f}'.format(correlation_coefficient_sports))
plt.xlabel('Age')
plt.ylabel('Income (Million $)')
plt.show()


import pandas as pd 


data_new = { 
    'Age': [40, 55, 38, 65, 47], 
    'Net_Worth_Billion': [3.1, 6.2, 1.5, 9.2, 3.9], 
    'Years_of_Education': [15, 19, 13, 21, 16], 
    'Number_of_Companies': [2, 3, 1, 4, 2] 
} 

df_new = pd.DataFrame(data_new)

correlation_matrix_new = df_new.corr() 

print("Correlation Matrix for new dataset:") 
print(correlation_matrix_new) 
