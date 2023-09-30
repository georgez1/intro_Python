# Задача 44:
# В ячейке ниже представлен код генерирующий DataFrame,
# которая состоит всего из 1 столбца.
# Ваша задача перевести его в one hot вид.
# Сможете ли вы это сделать без get_dummies?

import pandas as pd 
import numpy as np 
import random
 
lst = ['robot'] * 10
lst += ['human'] * 10
random.shuffle(lst)
data = pd.DataFrame({'whoAmI': lst})
print(data)
 
print('-'*30)

# Делаем без get_dummies:
data1 = pd.DataFrame(index=data.index)
data1['human'] = np.where(data['whoAmI'] == 'human', 1, 0)
data1['robot'] = np.where(data['whoAmI'] == 'robot', 1, 0)
print(data1)

print('-'*30)

# Делаем с get_dummies для проверки:
data2 = pd.get_dummies(data['whoAmI'])
print(data2)

print('-'*30)

# Сравниваем результаты:
print (data1.to_dict() == data2.to_dict())
