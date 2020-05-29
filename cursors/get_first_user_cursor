
declare
cursor c is select * from users;
begin
for user in c loop
if user.user_id = 1 then
dbms_output.put_line('User ID :' || user.user_id);
dbms_output.put_line('Username :' || user.username);
end if;
end loop;
end;
