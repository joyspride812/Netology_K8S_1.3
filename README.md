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
<img width="471" height="54" alt="image" src="https://github.com/user-attachments/assets/6e4b1e83-882d-4268-ae51-e61b83fdc837" />




