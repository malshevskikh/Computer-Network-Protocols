# Computer-Network-Protocols
<!-- UNIVERSITY LOGO -->
<div align="center">
  <a href="https://bmstu.ru">
    <img src="https://user-images.githubusercontent.com/67475107/225371733-8fd6f639-bf62-49bd-866c-4e08116fa20c.png" alt="University logo" height="200">
  </a>
  
  Developed by Maxim Alshevskikh (<a href="https://www.linkedin.com/in/maxim-alshevskikh-b473b42b3/">LinkedIn</a>)
  <br/>
</div>

<h2>Исследование работы сети между компьютерами при совпадении адресаций сетей в двух компаниях</h2>
<h3>Вы объединяете две компании с развитой региональной сетью офисов:</h3>
<ol>
  <li>Адресация сетей выбранных адиминистраторами совпали.</li>
  <li>Адреса настроены статически для всех узлов, полное изменение адресации невозможно.</li>
  <li>В каждой сети статическая маршрутизация.</li>
  <li>В каждой сети есть файловый сервер.</li>
  <li>В каждой сети определены компьютеры, к которым можно обратиться из другой сети, PC 1, PC 2, PC 3, PC 4.</li>
  <li>В каждой сети определены компьютеры, к которым можно обратиться из другой сети, PC 1, PC 2, PC 3, PC 4.</li>
  <li>Настроить статическую маршрутизацию.</li>
  <li>Исследовать работу сети, проверить результат связь между PC 1, PC 2, PC 3, PC 4.</li>
</ol>

<h3>Примерный вид сети:</h3>

![Снимок экрана 2025-04-11 193158](https://github.com/user-attachments/assets/8b48ac83-c65f-4c45-ba93-c28633fd207c)


<h3>Результаты работы:</h3>
<h2>Выполнение работы и исследование осуществлялись в виртуальной среде EVE-NG.</h2>
<h3>Для эмуляции работы сетевых устройств были использованы следующие образы:</h3>
<ol>
  <li>Virtual PC (VPCS) – используется в качестве компьютера; </li>
  <li>Cisco IOS 7206VXR (Dynamips) – используется в качестве маршрутизатора; </li>
</ol>

<h3>Вид сети, спроектированной в EVE_NG:</h3>

![image](https://github.com/user-attachments/assets/edca5659-1e24-4b56-b306-448921fadd1b)

<h3>Адресация сети:</h3>
| Сеть 192.168.1.0/24 |       |              |
|:-------------------:|:-----:|:------------:|
| Устройство          | Порт  | Адрес        |
| VPC PC1             | eth0  | 192.168.1.1  |
| VPC PC4             | eth0  | 192.168.1.1  |
| ROUTER1             | fa1/0 | 192.168.1.10 |
| ROUTER6             | fa1/0 | 192.168.1.10 |
| Сеть 192.168.4.0/24 |       |              |
| Устройство          | Порт  | Адрес        |
| VPC PC2             | eth0  | 192.168.4.1  |
| VPC PC3             | eth0  | 192.168.4.1  |
| ROUTER2             | fa1/0 | 192.168.4.10 |
| ROUTER5             | fa1/0 | 192.168.4.10 |
| Сеть 192.168.2.0/24 |       |              |
| Устройство          | Порт  | Адрес        |
| ROUTER1             | fa2/0 | 192.168.2.1  |
| ROUTER3             | fa1/0 | 192.168.2.2  |
| ROUTER6             | fa2/0 | 192.168.2.1  |
| ROUTER7             | fa1/0 | 192.168.2.2  |
| Сеть 192.168.3.0/24 |       |              |
| Устройство          | Порт  | Адрес        |
| ROUTER2             | fa2/0 | 192.168.3.3  |
| ROUTER3             | fa2/0 | 192.168.3.4  |
| ROUTER5             | fa2/0 | 192.168.3.3  |
| ROUTER7             | fa2/0 | 192.168.3.4  |
| Сеть 192.168.5.0/24 |       |              |
| Устройство          | Порт  | Адрес        |
| ROUTER3             | fa3/0 | 192.168.5.5  |
| ROUTER4             | fa1/0 | 192.168.5.6  |
| ROUTER7             | fa3/0 | 192.168.5.5  |
| ROUTER8             | fa1/0 | 192.168.5.6  |
| Сеть 100.0.1.0/8    |       |              |
| Устройство          | Порт  | Адрес        |
| ROUTER4             | fa2/0 | 100.0.0.1    |
| ROUTER8             | fa2/0 | 100.0.0.2    |

