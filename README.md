# space-objects-classification
Colab containing 3 models with 0.96, 0.96 and 0.95 accuracy classifying space objects

# ¿Cómo ejecutarlo?
Para obtener los mismos resultados es necesario ejecutar línea a línea del colab

# Nota
Hay una parte del código comentada:
# class1_data = data[data['target'] == 0]
# class2_data = data[data['target'] == 1]
# class3_data = data[data['target'] == 2]

# class1_sample = class1_data.sample(n=10000, random_state=42)
# class2_sample = class2_data.sample(n=10000, random_state=42)
# class3_sample = class3_data.sample(n=10000, random_state=42)

# reduced_data = pd.concat([class1_sample, class2_sample, class3_sample], axis=0)
# reduced_data = reduced_data.sample(frac=1, random_state=42).reset_index(drop=True)

# x = reduced_data.drop(['target'], axis = 1)
# y = reduced_data.loc[:,'target'].values

Esto se comentó pero el objetivo era reducir la data de 300000 muestras a 30000 para que los modelos no se demoraran tanto en ajustar los parámetros internos, en especial el **forward selection**. Sin embargo, cada modelo se demoró unos 20 minutos en ajustar.
Esto significa que el resultado final es de 30000 muestras y no del conjunto completo de 300000.
