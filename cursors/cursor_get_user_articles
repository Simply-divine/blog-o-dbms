declare
cursor c is select * from articles;
u_id users.user_id%type;
begin
u_id := :u_id;
for article in c loop
if article.creator_id = u_id then
dbms_output.put_line('Article ID :' || article.article_id);
dbms_output.put_line('title :' || article.title);
end if;
end loop;
end;
