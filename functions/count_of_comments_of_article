
DECLARE
comment_nums INT;
a_id articles.article_id%type;
n int;
FUNCTION num_of_comments RETURN INT IS total INT;
BEGIN
dbms_output.put_line('Enter article id: ');
a_id := :a_id; 
SELECT COUNT(*) INTO total
FROM comments
where article_id = a_id;
RETURN total;
END;
BEGIN
n:=num_of_comments();
dbms_output.put_line('Count of comments is '||n);
END;
