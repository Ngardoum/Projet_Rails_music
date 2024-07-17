# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
# Projet_Rails_music

1. Nombre total d'objets Album :

Album.count

2.Auteur de la chanson "White Room" :
Track.where(title: "White Room").pluck(:artist).first

3.Chanson qui dure exactement 188133 milliseconds :

Track.find_by(duration: 188133).title

4. Groupe ayant sorti l'album "Use Your Illusion II" :

Album.find_by(title: "Use Your Illusion II").artist


Requêtes SQL pour les questions de niveau moyen

1.Combien y a-t-il d'albums dont le titre contient "Great" ?

Album.where("title LIKE ?", "%Great%").count


2. Supprimer tous les albums dont le nom contient "music" :

Album.where("title LIKE ?", "%music%").destroy_all

3.Combien y a-t-il d'albums écrits par AC/DC ?

Album.where(artist: "AC/DC").count

4.Combien de chansons durent exactement 158589 millisecondes ?

Track.where(duration: 158589).count



