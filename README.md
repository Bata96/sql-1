--
-- PostgreSQL database dump
--

-- Dumped from database version 12.9 (Ubuntu 12.9-2.pgdg20.04+1)
-- Dumped by pg_dump version 12.9 (Ubuntu 12.9-2.pgdg20.04+1)

SET statement_timeout = 0;
SET lock_timeout = 0;
SET idle_in_transaction_session_timeout = 0;
SET client_encoding = 'UTF8';
SET standard_conforming_strings = on;
SELECT pg_catalog.set_config('search_path', '', false);
SET check_function_bodies = false;
SET xmloption = content;
SET client_min_messages = warning;
SET row_security = off;

DROP DATABASE universe;
--
-- Name: universe; Type: DATABASE; Schema: -; Owner: freecodecamp
--

CREATE DATABASE universe WITH TEMPLATE = template0 ENCODING = 'UTF8' LC_COLLATE = 'C.UTF-8' LC_CTYPE = 'C.UTF-8';


ALTER DATABASE universe OWNER TO freecodecamp;

\connect universe

SET statement_timeout = 0;
SET lock_timeout = 0;
SET idle_in_transaction_session_timeout = 0;
SET client_encoding = 'UTF8';
SET standard_conforming_strings = on;
SELECT pg_catalog.set_config('search_path', '', false);
SET check_function_bodies = false;
SET xmloption = content;
SET client_min_messages = warning;
SET row_security = off;

SET default_tablespace = '';

SET default_table_access_method = heap;

--
-- Name: description; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.description (
    name character varying(30) NOT NULL,
    opis text NOT NULL,
    drugi_opis text,
    treci_opis text,
    cetvrti_opis integer,
    description_id integer NOT NULL
);


ALTER TABLE public.description OWNER TO freecodecamp;

--
-- Name: description_description_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.description_description_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.description_description_id_seq OWNER TO freecodecamp;

--
-- Name: description_description_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.description_description_id_seq OWNED BY public.description.description_id;


--
-- Name: description_name_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.description_name_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.description_name_seq OWNER TO freecodecamp;

--
-- Name: description_name_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.description_name_seq OWNED BY public.description.name;


--
-- Name: galaxy; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.galaxy (
    name character varying(30) NOT NULL,
    has_life boolean,
    is_spherical boolean,
    planet_types text NOT NULL,
    distance_from_earth integer,
    galaxy_types integer,
    age_in_millions_of_years numeric,
    galaxy_id integer NOT NULL
);


ALTER TABLE public.galaxy OWNER TO freecodecamp;

--
-- Name: galaxy_galaxy_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.galaxy_galaxy_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.galaxy_galaxy_id_seq OWNER TO freecodecamp;

--
-- Name: galaxy_galaxy_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.galaxy_galaxy_id_seq OWNED BY public.galaxy.galaxy_id;


--
-- Name: galaxy_name_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.galaxy_name_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.galaxy_name_seq OWNER TO freecodecamp;

--
-- Name: galaxy_name_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.galaxy_name_seq OWNED BY public.galaxy.name;


--
-- Name: moon; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.moon (
    name character varying(30) NOT NULL,
    has_life boolean NOT NULL,
    is_spherical boolean,
    planet_types text NOT NULL,
    distance_from_earth integer,
    galaxy_types integer,
    age_in_millions_of_years numeric,
    moon_id integer NOT NULL
);


ALTER TABLE public.moon OWNER TO freecodecamp;

--
-- Name: moon_moon_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.moon_moon_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.moon_moon_id_seq OWNER TO freecodecamp;

--
-- Name: moon_moon_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.moon_moon_id_seq OWNED BY public.moon.moon_id;


--
-- Name: moon_name_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.moon_name_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.moon_name_seq OWNER TO freecodecamp;

--
-- Name: moon_name_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.moon_name_seq OWNED BY public.moon.name;


--
-- Name: planet; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.planet (
    has_life boolean NOT NULL,
    is_spherical boolean,
    planet_types text NOT NULL,
    distance_from_earth integer,
    galaxy_types integer,
    age_in_millions_of_years numeric,
    name character varying(30) NOT NULL,
    planet_id integer NOT NULL
);


ALTER TABLE public.planet OWNER TO freecodecamp;

--
-- Name: planet_name_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.planet_name_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.planet_name_seq OWNER TO freecodecamp;

--
-- Name: planet_name_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.planet_name_seq OWNED BY public.planet.name;


--
-- Name: planet_planet_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.planet_planet_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.planet_planet_id_seq OWNER TO freecodecamp;

--
-- Name: planet_planet_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.planet_planet_id_seq OWNED BY public.planet.planet_id;


--
-- Name: star; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.star (
    name character varying(30) NOT NULL,
    has_life boolean NOT NULL,
    is_spherical boolean,
    planet_types text NOT NULL,
    distance_from_earth integer,
    galaxy_types integer,
    age_in_millions_of_years numeric,
    star_id integer NOT NULL
);


ALTER TABLE public.star OWNER TO freecodecamp;

--
-- Name: star_name_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.star_name_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.star_name_seq OWNER TO freecodecamp;

--
-- Name: star_name_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.star_name_seq OWNED BY public.star.name;


--
-- Name: star_star_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.star_star_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.star_star_id_seq OWNER TO freecodecamp;

--
-- Name: star_star_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.star_star_id_seq OWNED BY public.star.star_id;


--
-- Name: description name; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.description ALTER COLUMN name SET DEFAULT nextval('public.description_name_seq'::regclass);


--
-- Name: description description_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.description ALTER COLUMN description_id SET DEFAULT nextval('public.description_description_id_seq'::regclass);


--
-- Name: galaxy name; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy ALTER COLUMN name SET DEFAULT nextval('public.galaxy_name_seq'::regclass);


--
-- Name: galaxy galaxy_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy ALTER COLUMN galaxy_id SET DEFAULT nextval('public.galaxy_galaxy_id_seq'::regclass);


--
-- Name: moon name; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon ALTER COLUMN name SET DEFAULT nextval('public.moon_name_seq'::regclass);


--
-- Name: moon moon_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon ALTER COLUMN moon_id SET DEFAULT nextval('public.moon_moon_id_seq'::regclass);


--
-- Name: planet name; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet ALTER COLUMN name SET DEFAULT nextval('public.planet_name_seq'::regclass);


--
-- Name: planet planet_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet ALTER COLUMN planet_id SET DEFAULT nextval('public.planet_planet_id_seq'::regclass);


--
-- Name: star name; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star ALTER COLUMN name SET DEFAULT nextval('public.star_name_seq'::regclass);


--
-- Name: star star_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star ALTER COLUMN star_id SET DEFAULT nextval('public.star_star_id_seq'::regclass);


--
-- Data for Name: description; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.description VALUES ('1', 'text', NULL, NULL, NULL, 1);
INSERT INTO public.description VALUES ('2', 'text', NULL, NULL, NULL, 2);
INSERT INTO public.description VALUES ('3', 'text', NULL, NULL, NULL, 3);


--
-- Data for Name: galaxy; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.galaxy VALUES ('1', true, true, 'planets', 1000, 1, 10000, 1);
INSERT INTO public.galaxy VALUES ('2', true, true, 'planets', 1000, 1, 10000, 2);
INSERT INTO public.galaxy VALUES ('3', true, true, 'planets', 1000, 1, 10000, 3);
INSERT INTO public.galaxy VALUES ('4', true, true, 'planets', 1000, 1, 10000, 4);
INSERT INTO public.galaxy VALUES ('5', true, true, 'planets', 1000, 1, 10000, 5);
INSERT INTO public.galaxy VALUES ('6', true, true, 'planets', 1000, 1, 10000, 6);


--
-- Data for Name: moon; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.moon VALUES ('1', false, false, 'planets', 1000, 1, 10000, 1);
INSERT INTO public.moon VALUES ('2', false, false, 'planets', 1000, 1, 10000, 2);
INSERT INTO public.moon VALUES ('3', false, false, 'planets', 1000, 1, 10000, 3);
INSERT INTO public.moon VALUES ('4', false, false, 'planets', 1000, 1, 10000, 4);
INSERT INTO public.moon VALUES ('5', false, false, 'planets', 1000, 1, 10000, 5);
INSERT INTO public.moon VALUES ('6', false, false, 'planets', 1000, 1, 10000, 6);
INSERT INTO public.moon VALUES ('7', false, false, 'planets', 1000, 1, 10000, 7);
INSERT INTO public.moon VALUES ('8', false, false, 'planets', 1000, 1, 10000, 8);
INSERT INTO public.moon VALUES ('9', false, false, 'planets', 1000, 1, 10000, 9);
INSERT INTO public.moon VALUES ('10', false, false, 'planets', 1000, 1, 10000, 10);
INSERT INTO public.moon VALUES ('11', false, false, 'planets', 1000, 1, 10000, 11);
INSERT INTO public.moon VALUES ('12', false, false, 'planets', 1000, 1, 10000, 12);
INSERT INTO public.moon VALUES ('13', false, false, 'planets', 1000, 1, 10000, 13);
INSERT INTO public.moon VALUES ('14', false, false, 'planets', 1000, 1, 10000, 14);
INSERT INTO public.moon VALUES ('15', false, false, 'planets', 1000, 1, 10000, 15);
INSERT INTO public.moon VALUES ('16', false, false, 'planets', 1000, 1, 10000, 16);
INSERT INTO public.moon VALUES ('17', false, false, 'planets', 1000, 1, 10000, 17);
INSERT INTO public.moon VALUES ('18', false, false, 'planets', 1000, 1, 10000, 18);
INSERT INTO public.moon VALUES ('19', false, false, 'planets', 1000, 1, 10000, 19);
INSERT INTO public.moon VALUES ('20', false, false, 'planets', 1000, 1, 10000, 20);


--
-- Data for Name: planet; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.planet VALUES (false, false, 'planets', 1000, 1, 10000, '1', 1);
INSERT INTO public.planet VALUES (false, false, 'planets', 1000, 1, 10000, '2', 2);
INSERT INTO public.planet VALUES (false, false, 'planets', 1000, 1, 10000, '3', 3);
INSERT INTO public.planet VALUES (false, false, 'planets', 1000, 1, 10000, '4', 4);
INSERT INTO public.planet VALUES (false, false, 'planets', 1000, 1, 10000, '5', 5);
INSERT INTO public.planet VALUES (false, false, 'planets', 1000, 1, 10000, '6', 6);
INSERT INTO public.planet VALUES (false, false, 'planets', 1000, 1, 10000, '7', 7);
INSERT INTO public.planet VALUES (false, false, 'planets', 1000, 1, 10000, '8', 8);
INSERT INTO public.planet VALUES (false, false, 'planets', 1000, 1, 10000, '9', 9);
INSERT INTO public.planet VALUES (false, false, 'planets', 1000, 1, 10000, '10', 10);
INSERT INTO public.planet VALUES (false, false, 'planets', 1000, 1, 10000, '11', 11);
INSERT INTO public.planet VALUES (false, false, 'planets', 1000, 1, 10000, '12', 12);


--
-- Data for Name: star; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.star VALUES ('1', false, false, 'planets', 1000, 1, 10000, 1);
INSERT INTO public.star VALUES ('2', false, false, 'planets', 1000, 1, 10000, 2);
INSERT INTO public.star VALUES ('3', false, false, 'planets', 1000, 1, 10000, 3);
INSERT INTO public.star VALUES ('4', false, false, 'planets', 1000, 1, 10000, 4);
INSERT INTO public.star VALUES ('5', false, false, 'planets', 1000, 1, 10000, 5);
INSERT INTO public.star VALUES ('6', false, false, 'planets', 1000, 1, 10000, 6);


--
-- Name: description_description_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.description_description_id_seq', 3, true);


--
-- Name: description_name_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.description_name_seq', 3, true);


--
-- Name: galaxy_galaxy_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.galaxy_galaxy_id_seq', 6, true);


--
-- Name: galaxy_name_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.galaxy_name_seq', 6, true);


--
-- Name: moon_moon_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.moon_moon_id_seq', 20, true);


--
-- Name: moon_name_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.moon_name_seq', 20, true);


--
-- Name: planet_name_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.planet_name_seq', 12, true);


--
-- Name: planet_planet_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.planet_planet_id_seq', 12, true);


--
-- Name: star_name_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.star_name_seq', 6, true);


--
-- Name: star_star_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.star_star_id_seq', 6, true);


--
-- Name: description description_name_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.description
    ADD CONSTRAINT description_name_key UNIQUE (name);


--
-- Name: description description_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.description
    ADD CONSTRAINT description_pkey PRIMARY KEY (description_id);


--
-- Name: galaxy galaxy_name_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy
    ADD CONSTRAINT galaxy_name_key UNIQUE (name);


--
-- Name: galaxy galaxy_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy
    ADD CONSTRAINT galaxy_pkey PRIMARY KEY (galaxy_id);


--
-- Name: moon moon_name_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon
    ADD CONSTRAINT moon_name_key UNIQUE (name);


--
-- Name: moon moon_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon
    ADD CONSTRAINT moon_pkey PRIMARY KEY (moon_id);


--
-- Name: planet planet_name_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT planet_name_key UNIQUE (name);


--
-- Name: planet planet_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT planet_pkey PRIMARY KEY (planet_id);


--
-- Name: star star_name_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT star_name_key UNIQUE (name);


--
-- Name: star star_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT star_pkey PRIMARY KEY (star_id);


--
-- Name: description description_description_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.description
    ADD CONSTRAINT description_description_id_fkey FOREIGN KEY (description_id) REFERENCES public.description(description_id);


--
-- Name: planet moon_id; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT moon_id FOREIGN KEY (planet_id) REFERENCES public.planet(planet_id);


--
-- Name: star planet_id; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT planet_id FOREIGN KEY (star_id) REFERENCES public.star(star_id);


--
-- Name: galaxy star_id; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy
    ADD CONSTRAINT star_id FOREIGN KEY (galaxy_id) REFERENCES public.galaxy(galaxy_id);


--
-- PostgreSQL database dump complete
--

