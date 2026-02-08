## Netology_K8S_1.3 (Моисеенко А.Н.)
  
## Задание 1. Создать Deployment и обеспечить доступ к репликам приложения из другого Pod
- Создать Deployment приложения, состоящего из двух контейнеров — nginx и multitool. Решить возникшую ошибку.
- После запуска увеличить количество реплик работающего приложения до 2.
- Продемонстрировать количество подов до и после масштабирования.
- Создать Service, который обеспечит доступ до реплик приложений из п.1.
- Создать отдельный Pod с приложением multitool и убедиться с помощью curl, что из пода есть доступ до приложений из п.1.

### Создание configmap для nginx в контейнере multitool
<img width="612" height="128" alt="image" src="https://github.com/user-attachments/assets/6134c5fe-9004-4c32-9441-fc7877f7eeaa" />



### Вывод kubectl apply -f deployment.yaml
<img width="554" height="55" alt="image" src="https://github.com/user-attachments/assets/ff443c01-d355-479c-9ffc-7696d142c975" />

### Вывод kubectl get deploy
<img width="470" height="55" alt="image" src="https://github.com/user-attachments/assets/e6b812ce-cbd3-4099-9be8-175407c8f017" />


### Вывод kubectl get pods
<img width="584" height="73" alt="image" src="https://github.com/user-attachments/assets/58c1a4cf-00dc-404d-85e7-6aa54d6e809c" />

### Увеличение количество реплик до двух
<img width="727" height="36" alt="image" src="https://github.com/user-attachments/assets/8437ffb8-6bdc-476a-b4e9-424bb39f8f00" />

### Вывод kubectl get pods с новым POD
<img width="523" height="73" alt="image" src="https://github.com/user-attachments/assets/ee0ae7c4-f47b-4673-8226-408d227ef811" />

### Создание сервиса web-service
<img width="589" height="139" alt="image" src="https://github.com/user-attachments/assets/2b05a690-8399-46a5-ba93-f25e960faaa0" />

### Создание отдельного POD multitool-pod
<img width="609" height="121" alt="image" src="https://github.com/user-attachments/assets/04d37be3-aa03-43bb-9601-af6ccc7f600a" />

### Проверка, что из пода mutitool-pod есть доступ до приложений (nginx) из сервиса web-service
<img width="834" height="401" alt="image" src="https://github.com/user-attachments/assets/5bcdcff8-5c64-497c-b143-25e5ec3f3ce1" />

## Задание 2. Создать Deployment и обеспечить старт основного контейнера при выполнении условий
- Создать Deployment приложения nginx и обеспечить старт контейнера только после того, как будет запущен сервис этого приложения.
- Убедиться, что nginx не стартует. В качестве Init-контейнера взять busybox.
- Создать и запустить Service. Убедиться, что Init запустился.
- Продемонстрировать состояние пода до и после запуска сервиса.

### Создание deployment c init контейнером.
<img width="669" height="133" alt="image" src="https://github.com/user-attachments/assets/3ad275bb-9f8e-44fc-8242-20cab0dfad12" />


### Лог  init контейнера wait-for-service. Контейнер не может разрешить DNS имя в ip адрес сервиса "nginx-service" и завершить цикл.
<img width="576" height="416" alt="image" src="https://github.com/user-attachments/assets/37c53670-28c7-49a0-9408-7d66cc6ed106" />

### Создание Сервиса nginx-service.
<img width="570" height="43" alt="image" src="https://github.com/user-attachments/assets/86ad1ade-1e30-490f-a5be-de97c8791f5e" />

### После создания сервиса контейнер nginx в POD nginx-init-76796d55b-rrdgq поднялся
<img width="573" height="110" alt="image" src="https://github.com/user-attachments/assets/817157fa-d74d-48a9-a8c5-6e08a33da4ac" />



















