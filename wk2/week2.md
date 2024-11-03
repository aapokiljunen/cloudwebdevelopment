---
title: "Viikko 2"
layout: default
---

## Viikko 2
### Jekyll-sivuston automaatio GitHub Actionsilla 
Github Actions mahdollistaa Jekyll-sivuston julkaisemisen automaattisesti, kun muutoksia pushataan main-haaraan. Työnkulkua voi määrittää .yml-tiedostolla, johon tallennetaan tarvittavat tiedot sivuston kääntämiseen ja julkaisemiseen. 

## CI/CD-putkisto rakentaminen web-sovellukselle
*Continuous integration, Continuous delivery (Continuous deployment)*

Ajatuksena putkiston rakentamisessa on luoda joustava ja tehokas kehitysympäristö, jossa sovellusta kehitetään nopealla syklillä pienin askelin, vaihtoehtona harvemmille isoille päivityksille. CI/CD-putkisto tarvitsee versionhallinnan, jossa päivityksen vieminen päähaaraan laukaisee CI/CD-putkiston. Idea on, että päivityksen jälkeen ajetaan kattava sarja testejä, jotka varmistavat ohjelman toimintakyvyn ja sen jälkeen sovellus julkaistaan mahdollisesti automaattisesti. Esimerkiksi ohjelmistoja CI/CD-putkiston hallintaan ovat Jenkins, GitLab CI/CD, GitHub Actions, CircleCI ja Travis CI. Testausympäristön hallintaan on puolestaan omat ohjelmasa, joilla testausta voidaan hallita erilaisissa ympäristöissä.


[Palaa etusivulle](../index.md)