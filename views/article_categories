
create or replace view article_comments_full as
    select articles.article_id, title, comment_description as comments, username as commentor
    from articles, comments, users
    where comments.article_id = articles.article_id
    and comments.commentor_id = users.user_id
    order by articles.title;

