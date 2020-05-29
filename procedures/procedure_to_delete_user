declare
    row_present number;
    u_id users.user_id%type;
procedure deleteUser is 
begin
        dbms_output.put_line('Enter User Id');
        u_id := :u_id;
        dbms_output.put_line('    User ID:'||u_id);
        row_present := 0;
        select count(*)
        into row_present
        from users
        where users.user_id=u_id;
        if row_present = 0 then
            RAISE_APPLICATION_ERROR(-20001,'User Id is not present');
        else
            delete from users where users.user_id=u_id;
        end if;
end;
begin
    deleteUser;
end;
