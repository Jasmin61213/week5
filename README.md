# week5

## optional
```sql
create table message(
    ->id bigint primary key auto_increment,
    ->member_id bigint not null,
    ->content varchar(255) not null,
    ->like_count int unsigned not null default 0,
    ->time datetime not null default current_timestamp,
    ->foreign key(member_id) references member(id) on delete cascade
);
```
<img width="592" alt="image" src="https://user-images.githubusercontent.com/110441965/198873633-99e6cde5-f75f-4bf8-8f36-5310e6901ed8.png">

```sql
select member.name,message.content from member
inner join message
on member.id=message.member_id;
```
<img width="386" alt="image" src="https://user-images.githubusercontent.com/110441965/198873506-114263a5-9330-49e4-8f49-711bb50efd92.png">

```sql
select member.name,message.content from member
inner join message
on member.id=message.member_id
and username='test';
```
<img width="398" alt="image" src="https://user-images.githubusercontent.com/110441965/198873528-8d6fc5ef-46c9-4936-b9ea-655967dec6cf.png">

```sql
select avg(message.like_count) from member
inner join message
on member.id=message.member_id
and username='test';
```
<img width="372" alt="image" src="https://user-images.githubusercontent.com/110441965/198873543-ac0180cf-1c5c-471a-9ab9-085c9d02dd9d.png">


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
