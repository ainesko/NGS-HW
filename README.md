# NGS-HW1

Google Colab: https://colab.research.google.com/drive/15eYjtbpV0RkbrPzaxSwxTu2jDqAKL5sh?usp=sharing


# Задание 1

## Проведём анализ для исходных последовательностей

### 100x.1

***GC-content***

FastQC

![image](https://user-images.githubusercontent.com/93263861/154988874-74d75a6c-1987-4873-94d6-083bcc994e15.png)

Результат запуска программы

![image](https://user-images.githubusercontent.com/93263861/154989115-1caded84-c3cb-4fe2-8967-ce05afdc86f2.png)




### 100x.2

***GC-content***

FastQC

![image](https://user-images.githubusercontent.com/93263861/154989230-2aabd13d-c303-4e4f-af06-0e4cb22f2bf1.png)

Результат запуска программы

![image](https://user-images.githubusercontent.com/93263861/154989263-2c1e0b60-2e55-4f7d-9c61-c93d2967f2b7.png)

В обоих случаях самодельный график сильно совпадает с результатом FastQC.

## Фильтрация ридов

***Будем рассматривать нуклеотиды с вероятностью ошибки < 10%. Отберём риды, в которых рассматриваемых нуклеотидов хотя бы 90%.***

### 100x.1

![image](https://user-images.githubusercontent.com/93263861/155130893-e7cb04bf-4411-4ce9-ba74-f98d392e525f.png)


### 100x.2

![image](https://user-images.githubusercontent.com/93263861/155130835-70eb7f4d-4027-48f1-bd7b-081e77c6fda0.png)



# Задание 2

### 100x.1

FastQC

![image](https://user-images.githubusercontent.com/93263861/155122094-5c20dbdf-6e3c-4d8b-865d-fa0f2198a59e.png)

Результат запуска программы

![image](https://user-images.githubusercontent.com/93263861/155131360-5176a3b9-3ae5-4d4f-b8ac-5a9d33e34252.png)


### 100x.2

FastQC

![image](https://user-images.githubusercontent.com/93263861/155121762-8a846833-9b32-45c3-b983-1d98336a44be.png)

Результат запуска программы

![image](https://user-images.githubusercontent.com/93263861/155131392-2e6b610f-0d08-413e-87e7-a74e5f681c75.png)


Поскольку графики показывают немного разные вещи (один зависимость вероятности P ошибки от позиции нуклеотида, другой - Phred score Q данной позиции), то сравнивать их непосредственно не имеет смысла. Но с учётом преобразования P = 10^(-Q/10) графики очень похожи. На каждом графике наблюдается увеличение вероятности ошибки к концу рида, что является характерным для Illumina.


