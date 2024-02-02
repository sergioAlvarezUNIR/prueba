CREATE DATABASE "library-books"
  WITH ENCODING='UTF8'
       OWNER=postgres
       LC_COLLATE='Spanish_Colombia.1252'
       LC_CTYPE='Spanish_Colombia.1252'
       CONNECTION LIMIT=-1
       TABLESPACE=pg_default;

 CREATE TABLE public.books
(
  isbn character varying(13) NOT NULL,
  title character varying(150),
  category character varying(60),
  author character varying(80),
  page_count integer DEFAULT 0,
  description character varying(250),
  CONSTRAINT books_pkey PRIMARY KEY (isbn)
)
WITH (
  OIDS=FALSE
);
ALTER TABLE public.books
  OWNER TO postgres;
