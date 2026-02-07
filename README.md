## Netology_K8S_1.3 (Моисеенко А.Н.)
  
## Задание 1. Создать Deployment и обеспечить доступ к репликам приложения из другого Pod
- Создать Deployment приложения, состоящего из двух контейнеров — nginx и multitool. Решить возникшую ошибку.
- После запуска увеличить количество реплик работающего приложения до 2.
- Продемонстрировать количество подов до и после масштабирования.
- Создать Service, который обеспечит доступ до реплик приложений из п.1.
- Создать отдельный Pod с приложением multitool и убедиться с помощью curl, что из пода есть доступ до приложений из п.1.

### Создание configmap для nginx в контейнере multitool
<img width="912" height="40" alt="image" src="https://github.com/user-attachments/assets/0d7d851e-4bac-426e-ac82-0143eb8b04f9" />


### Вывод kubectl apply -f deployment.yaml
<img width="554" height="55" alt="image" src="https://github.com/user-attachments/assets/ff443c01-d355-479c-9ffc-7696d142c975" />

### Вывод kubectl get deploy
<img width="470" height="55" alt="image" src="https://github.com/user-attachments/assets/e6b812ce-cbd3-4099-9be8-175407c8f017" />


### Вывод kubectl get pods
<img width="584" height="73" alt="image" src="https://github.com/user-attachments/assets/58c1a4cf-00dc-404d-85e7-6aa54d6e809c" />

### Увеличение количество реплик до двух
<img width="727" height="36" alt="image" src="https://github.com/user-attachments/assets/8437ffb8-6bdc-476a-b4e9-424bb39f8f00" />
### Вывод kubectl get pods с новым POD
<img width="670" height="91" alt="image" src="https://github.com/user-attachments/assets/4cc2a2e9-d25e-48f8-b95e-7ea8c46bf494" />







