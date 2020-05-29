
create or replace trigger username_check
before insert or update on users
for each row
begin
    if length(:NEW.username) > 10 or length(:NEW.username) < 3 then
     RAISE_APPLICATION_ERROR (-20001,'username should be between 3 to 10 characters');
    end if;
end;
