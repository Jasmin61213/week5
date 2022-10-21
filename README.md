# week5

## 要求三
``` sql
insert into member (name,username,password)
values ('test','test','test');
```
![1](https://user-images.githubusercontent.com/110441965/197242571-50c35832-1826-4227-9c39-af0ec243920e.jpg)
``` sql
select * from member;
``` 
![2](https://user-images.githubusercontent.com/110441965/197242820-dfc7c117-f63a-49c4-84d2-f50bc4ff890f.jpg)
``` sql
select * from member order by time desc;
```
![3](https://user-images.githubusercontent.com/110441965/197242869-6b8638a0-152e-4f59-85eb-88fc377ff086.jpg)
``` sql
select * from member order by time desc limit 1, 3;
```
![4](https://user-images.githubusercontent.com/110441965/197242917-89ff37f4-6d3a-4d20-a7f5-4ba7098ec913.jpg)
``` sql
select * from member where username='test';
```
![5](https://user-images.githubusercontent.com/110441965/197243016-b39a8cbd-95a1-4c75-9fa1-71a5c90d2270.jpg)
``` sql
select * from member where username='test' and password='test';
```
![6](https://user-images.githubusercontent.com/110441965/197243104-b71518ca-d845-4016-bde8-4cb30e68b6ae.jpg)
``` sql
update member set name='test2' where username='test';
```
![7](https://user-images.githubusercontent.com/110441965/197243165-1f5d5527-6e18-48b5-b82a-7a4da131e36e.jpg)

## 要求四
``` sql
select count(*) from member;
```
![8](https://user-images.githubusercontent.com/110441965/197243309-f57e44bf-7c69-44bf-beb9-cda919ac580e.jpg)
``` sql
select sum(follower_count) from member;
```
![9](https://user-images.githubusercontent.com/110441965/197243427-e869343a-1d76-49cd-91b2-d67a16ff5105.jpg)
``` sql
select avg(follower_count) from member;
```
![10](https://user-images.githubusercontent.com/110441965/197243496-be38ab0f-954b-43c4-ab24-2d02887f2008.jpg)
