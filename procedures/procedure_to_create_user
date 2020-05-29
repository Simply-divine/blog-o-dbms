declare
    user_id users.user_id%type;
    row_present number;
    username users.username%type;
    email users.email%type;
    psw users.password%type;
procedure createUser is 
begin
    dbms_output.put_line('Enter id');
    row_present := 0;
    user_id := :user_id;
    dbms_output.put_line('    User ID:'||user_id);
    select count(*)
    into row_present
    from users
    where users.user_id = user_id;
    if row_present = 1 then
        RAISE_APPLICATION_ERROR(-20001, 'User already present');
    else
        dbms_output.put_line('Enter username');
        username := :username;
        dbms_output.put_line('    Username:'||username);
        dbms_output.put_line('Enter email: ');
        email := :email;
        dbms_output.put_line('    email: '||email);
        psw := :psw;
        insert into users(user_id,username,email,password) values(user_id,username,email,psw);
    end if;
end;
begin
    createUser;
end;
