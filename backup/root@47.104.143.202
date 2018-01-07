-- MySQL dump 10.13  Distrib 5.7.19, for macos10.12 (x86_64)
--
-- Host: localhost    Database: tale
-- ------------------------------------------------------
-- Server version	5.7.19

/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8 */;
/*!40103 SET @OLD_TIME_ZONE=@@TIME_ZONE */;
/*!40103 SET TIME_ZONE='+00:00' */;
/*!40014 SET @OLD_UNIQUE_CHECKS=@@UNIQUE_CHECKS, UNIQUE_CHECKS=0 */;
/*!40014 SET @OLD_FOREIGN_KEY_CHECKS=@@FOREIGN_KEY_CHECKS, FOREIGN_KEY_CHECKS=0 */;
/*!40101 SET @OLD_SQL_MODE=@@SQL_MODE, SQL_MODE='NO_AUTO_VALUE_ON_ZERO' */;
/*!40111 SET @OLD_SQL_NOTES=@@SQL_NOTES, SQL_NOTES=0 */;

--
-- Table structure for table `t_attach`
--

DROP TABLE IF EXISTS `t_attach`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!40101 SET character_set_client = utf8 */;
CREATE TABLE `t_attach` (
  `id` int(11) unsigned NOT NULL AUTO_INCREMENT,
  `fname` varchar(100) NOT NULL DEFAULT '',
  `ftype` varchar(50) DEFAULT '',
  `fkey` varchar(100) NOT NULL DEFAULT '',
  `author_id` int(10) DEFAULT NULL,
  `created` int(10) NOT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=2 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `t_attach`
--

LOCK TABLES `t_attach` WRITE;
/*!40000 ALTER TABLE `t_attach` DISABLE KEYS */;
INSERT INTO `t_attach` VALUES (1,'TB2NGumfwvD8KJjSsplXXaIEFXa_!!2202264386.jpg_400x400.jpg','image','/upload/2018/01/7e7aks6ki6hononi42buc6t759.jpg',1,1515223714);
/*!40000 ALTER TABLE `t_attach` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `t_comments`
--

DROP TABLE IF EXISTS `t_comments`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!40101 SET character_set_client = utf8 */;
CREATE TABLE `t_comments` (
  `coid` int(10) unsigned NOT NULL AUTO_INCREMENT,
  `cid` int(10) unsigned DEFAULT '0',
  `created` int(10) unsigned DEFAULT '0',
  `author` varchar(200) DEFAULT NULL,
  `author_id` int(10) unsigned DEFAULT '0',
  `owner_id` int(10) unsigned DEFAULT '0',
  `mail` varchar(200) DEFAULT NULL,
  `url` varchar(200) DEFAULT NULL,
  `ip` varchar(64) DEFAULT NULL,
  `agent` varchar(200) DEFAULT NULL,
  `content` text,
  `type` varchar(16) DEFAULT 'comment',
  `status` varchar(16) DEFAULT 'approved',
  `parent` int(10) unsigned DEFAULT '0',
  PRIMARY KEY (`coid`),
  KEY `cid` (`cid`),
  KEY `created` (`created`)
) ENGINE=InnoDB AUTO_INCREMENT=3 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `t_comments`
--

LOCK TABLES `t_comments` WRITE;
/*!40000 ALTER TABLE `t_comments` DISABLE KEYS */;
INSERT INTO `t_comments` VALUES (1,3,1515223983,'111',0,1,'280887262@qq.com','','0:0:0:0:0:0:0:1',NULL,'评论123123123213','comment','approved',0),(2,3,1515233770,'111',0,1,'280887262@qq.com',NULL,'0:0:0:0:0:0:0:1',NULL,'1\r\n1\r\n1\r\n1\r\n1\r\n1\r\n\r\n1\r\n1\r\n1\r\n1\r\n1\r\n1\r\n1\r\n\r\n\r\n1\r\n1\r\n1\r\n1','comment','approved',0);
/*!40000 ALTER TABLE `t_comments` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `t_contents`
--

DROP TABLE IF EXISTS `t_contents`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!40101 SET character_set_client = utf8 */;
CREATE TABLE `t_contents` (
  `cid` int(10) unsigned NOT NULL AUTO_INCREMENT,
  `title` varchar(200) DEFAULT NULL,
  `slug` varchar(200) DEFAULT NULL,
  `created` int(10) unsigned DEFAULT '0',
  `modified` int(10) unsigned DEFAULT '0',
  `content` text COMMENT '内容文字',
  `author_id` int(10) unsigned DEFAULT '0',
  `type` varchar(16) DEFAULT 'post',
  `status` varchar(16) DEFAULT 'publish',
  `tags` varchar(200) DEFAULT NULL,
  `categories` varchar(200) DEFAULT NULL,
  `hits` int(10) unsigned DEFAULT '0',
  `comments_num` int(10) unsigned DEFAULT '0',
  `allow_comment` tinyint(1) DEFAULT '1',
  `allow_ping` tinyint(1) DEFAULT '1',
  `allow_feed` tinyint(1) DEFAULT '1',
  PRIMARY KEY (`cid`),
  UNIQUE KEY `slug` (`slug`),
  KEY `created` (`created`)
) ENGINE=InnoDB AUTO_INCREMENT=4 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `t_contents`
--

LOCK TABLES `t_contents` WRITE;
/*!40000 ALTER TABLE `t_contents` DISABLE KEYS */;
INSERT INTO `t_contents` VALUES (1,'关于我','about',1487853610,1515237728,'### 网站名称\r\n幺刀的博客\r\n### 初衷\r\n用于技术学习的心得记录\r\n### 自我描述\r\n估计要把此生浪费在永无止境的编程技术上了\r\n### 网站地址\r\nhttp://blog.hanshuai.xin</code></pre>\r\n### 我的邮箱\r\n280887262@qq.com',1,'page','publish',NULL,NULL,7,0,1,1,1),(2,'Hello My Blog',NULL,1487861184,1487872798,'## Hello  World.\r\n\r\n> ...\r\n\r\n----------\r\n\r\n\r\n<!--more-->\r\n\r\n```java\r\npublic static void main(String[] args){\r\n    System.out.println(\"Hello 13 Blog.\");\r\n}\r\n```',1,'post','publish','','default',25,0,1,1,1),(3,'test标题','my-first-article',1515223567,1515223628,'测试文章',1,'post','publish','标签','default',34,2,1,1,1);
/*!40000 ALTER TABLE `t_contents` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `t_logs`
--

DROP TABLE IF EXISTS `t_logs`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!40101 SET character_set_client = utf8 */;
CREATE TABLE `t_logs` (
  `id` int(11) unsigned NOT NULL AUTO_INCREMENT,
  `action` varchar(100) DEFAULT NULL,
  `data` varchar(2000) DEFAULT NULL,
  `author_id` int(10) DEFAULT NULL,
  `ip` varchar(20) DEFAULT NULL,
  `created` int(10) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=21 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `t_logs`
--

LOCK TABLES `t_logs` WRITE;
/*!40000 ALTER TABLE `t_logs` DISABLE KEYS */;
INSERT INTO `t_logs` VALUES (1,'登录后台',NULL,1,'127.0.0.1',1515223439),(2,'保存系统设置','{\"social_zhihu\":\"\",\"social_github\":\"qcxiao\",\"social_twitter\":\"\",\"social_weibo\":\"\"}',1,'127.0.0.1',1515223831),(3,'保存系统设置','{\"social_zhihu\":\"\",\"social_github\":\"qcxiao\",\"social_twitter\":\"\",\"social_weibo\":\"\"}',1,'127.0.0.1',1515223877),(4,'保存系统设置','{\"site_record\":\"\",\"site_description\":\"估计要把此生浪费在永无止境的编程技术上了\",\"site_title\":\"幺刀的博客\",\"site_theme\":\"default\",\"allow_install\":\"\"}',1,'127.0.0.1',1515224296),(5,'保存系统设置','{\"site_record\":\"\",\"site_description\":\"估计要把此生浪费在永无止境的编程技术上了\",\"site_title\":\"幺刀的博客\",\"site_theme\":\"default\",\"allow_install\":\"\"}',1,'127.0.0.1',1515224312),(6,'系统备份',NULL,1,'127.0.0.1',1515224419),(7,'系统备份',NULL,1,'127.0.0.1',1515224466),(8,'登录后台',NULL,1,'127.0.0.1',1515225255),(9,'系统备份',NULL,1,'127.0.0.1',1515226124),(10,'系统备份',NULL,1,'127.0.0.1',1515226130),(11,'系统备份',NULL,1,'127.0.0.1',1515226149),(12,'系统备份',NULL,1,'127.0.0.1',1515226149),(13,'系统备份',NULL,1,'127.0.0.1',1515226150),(14,'系统备份',NULL,1,'127.0.0.1',1515226155),(15,'保存系统设置','{\"site_record\":\"\",\"site_description\":\"估计要把此生浪费在永无止境的编程技术上了\",\"site_title\":\"幺刀的博客\",\"site_theme\":\"default\",\"allow_install\":\"\"}',1,'127.0.0.1',1515226205),(16,'登录后台',NULL,1,'127.0.0.1',1515227681),(17,'登录后台',NULL,1,'127.0.0.1',1515230222),(18,'登录后台',NULL,1,'127.0.0.1',1515233820),(19,'登录后台',NULL,1,'127.0.0.1',1515236269),(20,'登录后台',NULL,1,'127.0.0.1',1515238350);
/*!40000 ALTER TABLE `t_logs` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `t_metas`
--

DROP TABLE IF EXISTS `t_metas`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!40101 SET character_set_client = utf8 */;
CREATE TABLE `t_metas` (
  `mid` int(10) unsigned NOT NULL AUTO_INCREMENT,
  `name` varchar(200) DEFAULT NULL,
  `slug` varchar(200) DEFAULT NULL,
  `type` varchar(32) NOT NULL DEFAULT '',
  `description` varchar(200) DEFAULT NULL,
  `sort` int(10) unsigned DEFAULT '0',
  `parent` int(10) unsigned DEFAULT '0',
  PRIMARY KEY (`mid`),
  KEY `slug` (`slug`)
) ENGINE=InnoDB AUTO_INCREMENT=12 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `t_metas`
--

LOCK TABLES `t_metas` WRITE;
/*!40000 ALTER TABLE `t_metas` DISABLE KEYS */;
INSERT INTO `t_metas` VALUES (1,'default',NULL,'category',NULL,0,0),(6,'my github','https://github.com/qcxiao','link','',1,0),(7,'标签','标签','tag',NULL,0,0),(8,'Java',NULL,'category',NULL,0,0),(9,'专栏','https://xiaozhuanlan.com/','link','',0,0),(10,'My-Blog','http://13blog.site/','link','',0,0),(11,'云收藏','http://favorites.ren/','link','',0,0);
/*!40000 ALTER TABLE `t_metas` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `t_options`
--

DROP TABLE IF EXISTS `t_options`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!40101 SET character_set_client = utf8 */;
CREATE TABLE `t_options` (
  `name` varchar(32) NOT NULL DEFAULT '',
  `value` varchar(1000) DEFAULT '',
  `description` varchar(200) DEFAULT NULL,
  PRIMARY KEY (`name`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `t_options`
--

LOCK TABLES `t_options` WRITE;
/*!40000 ALTER TABLE `t_options` DISABLE KEYS */;
INSERT INTO `t_options` VALUES ('allow_install','',NULL),('site_description','估计要把此生浪费在永无止境的编程技术上了',NULL),('site_keywords','13 Blog',NULL),('site_record','','备案号'),('site_theme','default',NULL),('site_title','幺刀的博客',''),('social_github','qcxiao',NULL),('social_twitter','',NULL),('social_weibo','',NULL),('social_zhihu','',NULL);
/*!40000 ALTER TABLE `t_options` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `t_relationships`
--

DROP TABLE IF EXISTS `t_relationships`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!40101 SET character_set_client = utf8 */;
CREATE TABLE `t_relationships` (
  `cid` int(10) unsigned NOT NULL,
  `mid` int(10) unsigned NOT NULL,
  PRIMARY KEY (`cid`,`mid`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `t_relationships`
--

LOCK TABLES `t_relationships` WRITE;
/*!40000 ALTER TABLE `t_relationships` DISABLE KEYS */;
INSERT INTO `t_relationships` VALUES (2,1),(3,1),(3,7);
/*!40000 ALTER TABLE `t_relationships` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `t_users`
--

DROP TABLE IF EXISTS `t_users`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!40101 SET character_set_client = utf8 */;
CREATE TABLE `t_users` (
  `uid` int(10) unsigned NOT NULL AUTO_INCREMENT,
  `username` varchar(32) DEFAULT NULL,
  `password` varchar(64) DEFAULT NULL,
  `email` varchar(200) DEFAULT NULL,
  `home_url` varchar(200) DEFAULT NULL,
  `screen_name` varchar(32) DEFAULT NULL,
  `created` int(10) unsigned DEFAULT '0',
  `activated` int(10) unsigned DEFAULT '0',
  `logged` int(10) unsigned DEFAULT '0',
  `group_name` varchar(16) DEFAULT 'visitor',
  PRIMARY KEY (`uid`),
  UNIQUE KEY `name` (`username`),
  UNIQUE KEY `mail` (`email`)
) ENGINE=InnoDB AUTO_INCREMENT=2 DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `t_users`
--

LOCK TABLES `t_users` WRITE;
/*!40000 ALTER TABLE `t_users` DISABLE KEYS */;
INSERT INTO `t_users` VALUES (1,'admin','a66abb5684c45962d887564f08346e8d','1034683568@qq.com',NULL,'admin',1490756162,0,0,'visitor');
/*!40000 ALTER TABLE `t_users` ENABLE KEYS */;
UNLOCK TABLES;
/*!40103 SET TIME_ZONE=@OLD_TIME_ZONE */;

/*!40101 SET SQL_MODE=@OLD_SQL_MODE */;
/*!40014 SET FOREIGN_KEY_CHECKS=@OLD_FOREIGN_KEY_CHECKS */;
/*!40014 SET UNIQUE_CHECKS=@OLD_UNIQUE_CHECKS */;
/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
/*!40111 SET SQL_NOTES=@OLD_SQL_NOTES */;

-- Dump completed on 2018-01-07  0:08:58
