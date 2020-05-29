
create or replace trigger password_check
before insert or update on users
for each row
begin
    if length(:NEW.password) < 3 then
     RAISE_APPLICATION_ERROR (-20001,'password too short');
    end if;
end;
