DECLARE
u_id number;
FUNCTION max_posts_user RETURN integer IS id integer;
BEGIN
SELECT users.user_id into id
FROM users join (SELECT creator_id,count(*) as article from articles group by creator_id)post  on users.user_id=post.creator_id 
WHERE post.article=(SELECT MAX(article) from (SELECT count(*) as article from articles group by creator_id)) ;
RETURN id;
END;
BEGIN
u_id:=max_posts_user();
dbms_output.put_line('User having maximum posts is '||u_id);
END;
