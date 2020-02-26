---
title: Entity Common Data Service
description: Microsoft Dynamics 365 Human Resources používá Common Data Service k povolení scénářů rozšiřitelnosti a integrace.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 85dd95e8209fff28f214986f7960372db200351b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008403"
---
# <a name="common-data-service-entities"></a>Entity Common Data Service

Microsoft Dynamics 365 Human Resources používá Common Data Service k povolení scénářů rozšiřitelnosti a integrace.

Další informace týkající se Common Data Service získáte v tématu [Co je Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

V Common Data Service jsou k dispozici následující entity lidských zdrojů.

## <a name="benefit-entities"></a>Entity zaměstnaneckých výhod

**Interval provádění výpočtu zaměstnaneckých výhod**

| **Pole**        | **Datový typ** | **Požadováno** | **Lze prohledávat** |
|-------------------|---------------|--------------|----------------|
| Popis       | Text          |              | X              |
| Kontrola frekvence | Sada možností    | X            | X              |
| Lze ztlumit      | Dvě možnosti   |              | X              |
| Název              | Text          | X            | X              |


**Sazba výpočtu zaměstnanecké výhody**

| **Pole**  | **Datový typ** | **Požadováno** | **Lze prohledávat** |
|-------------|---------------|--------------|----------------|
| Popis | Text          |              | X              |
| Název        | Text          | X            | X              |
| TierType    | Sada možností    | X            | X              |


**Podrobnosti sazby výpočtu zaměstnanecké výhody**

| **Pole**                             | **Datový typ**  | **Požadováno** | **Lze prohledávat** |
|----------------------------------------|----------------|--------------|----------------|
| Číslo podrobností sazby výpočtu zaměstnanecké výhody | Text           | X            | X              |
| ID sazby pro výpočet                    | Vyhledávání         | X            | X              |
| Způsob určení příspěvku                    | Sada možností     | X            | X              |
| Účinné:                              | Pouze datum      | X            | X              |
| Zaměstnavatelský příspěvek                  | Desetinné číslo |              | X              |
| Vypršení platnosti                             | Pouze datum      | X            | X              |
| Odpočet pro pracovníka                        | Desetinné číslo |              | X              |


**Typ zaměstnanecké výhody**

| **Pole**           | **Datový typ** | **Požadováno** | **Lze prohledávat** |
|----------------------|---------------|--------------|----------------|
| Souběžná registrace | Sada možností    |              | X              |
| Popis          | Text          |              | X              |
| Název                 | Text          | X            | X              |
| Kategorie mzdy      | Sada možností    |              | X              |


**Plán zaměstnaneckých výhod**

| **Pole**                               | **Datový typ**  | **Požadováno** | **Lze prohledávat** |
|------------------------------------------|----------------|--------------|----------------|
| Způsob určení limitu                      | Sada možností     |              | X              |
| Typ zaměstnanecké výhody                             | Vyhledávání         | X            | X              |
| Způsob určení příspěvku                | Sada možností     |              | X              |
| Způsob určení příspěvku                      | Sada možností     |              | X              |
| Měna                                 | Vyhledávání         |              | X              |
| Priorita odpočtu                       | Celé číslo   |              | X              |
| Výchozí částka limitu příspěvku        | Měna       |              | X              |
| Částka limitu výchozího příspěvku (základní) | Měna       |              | X              |
| Výchozí období limitu příspěvku        | Sada možností     |              | X              |
| Výchozí limit částek odpočtu           | Měna       |              | X              |
| Částka limitu výchozího odpočtu (základní)    | Měna       |              | X              |
| Výchozí období limitu odpočtu           | Sada možností     |              | X              |
| Popis                              | Text           |              | X              |
| Směnný kurz                            | Desetinné číslo |              | X              |
| Je další spuštění zúčtování mezd                | Dvě možnosti    |              | X              |
| Je vykazovatelné provedení dostupné péče        | Dvě možnosti    |              | X              |
| Je generována nedoplatek                      | Dvě možnosti    |              | X              |
| Jde o hrubou částku                              | Dvě možnosti    |              | X              |
| Je primární                               | Dvě možnosti    |              | X              |
| Název                                     | Text           | X            | X              |
| Dopad mzdy                           | Sada možností     |              | X              |
| Typ odchodu do penze                          | Sada možností     |              | X              |


**Entita zaměstnání**

| **Pole**                     | **Datový typ**  | **Požadováno** | **Lze prohledávat** |
|--------------------------------|----------------|--------------|----------------|
| Upravené počáteční datum pracovníka     | Datum a čas  |              | X              |
| Společnost                        | Vyhledávání         | X            | X              |
| Částka jednotky oznámení zaměstnavatele | Desetinné číslo |              | X              |
| Jednotka oznámení zaměstnavatele        | Sada možností     |              | X              |
| Koncové datum zaměstnání            | Datum a čas  |              | X              |
| Číslo zaměstnání              | Text           | X            | X              |
| Počáteční datum zaměstnání          | Datum a čas  |              | X              |
| Datum posledního pracovního dne              | Datum a čas  |              | X              |
| Datum přechodu                | Datum a čas  |              | X              |
| Platné od                     | Datum a čas  | X            | X              |
| Platné do                       | Datum a čas  |              | X              |
| Pracovní podproces                         | Vyhledávání         | X            | X              |
| Částka oznámení pracovníka           | Desetinné číslo |              | X              |
| Počáteční datum pracovníků             | Datum a čas  |              | X              |
| Typ pracovníka                    | Sada možností     | X            | X              |
| Jednotka oznámení pracovníka          | Sada možností     |              | X              |

## <a name="worker-entities"></a>Entity pracovníků

**Etnický původ**

| **Pole**         | **Datový typ** | **Požadováno** | **Lze prohledávat** |
|--------------------|---------------|--------------|----------------|
| Popis        | Text          |              | X              |
| Název etnického původu | Text          | X            | X              |


**Jazyk**

| **Pole**    | **Datový typ** | **Požadováno** | **Lze prohledávat** |
|---------------|---------------|--------------|----------------|
| Popis   | Text          |              | X              |
| Název jazyka | Text          | X            | X              |


**Statut veterána**

| **Pole**           | **Datový typ** | **Požadováno** | **Lze prohledávat** |
|----------------------|---------------|--------------|----------------|
| Popis          | Text          |              | X              |
| Je chráněný válečný invalida | Dvě možnosti    |              | X              |
| Název jazyka        | Text          | X            | X              |


**Pracovní podproces**

| **Pole**                | **Datový typ** | **Požadováno** | **Lze prohledávat** |
|---------------------------|---------------|--------------|----------------|
| Datum narození                 | Pouze datum     |              | X              |
| Popis               | Text          |              | X              |
| E-mailová adresa 1           | E-mail         |              | X              |
| E-mailová adresa 2           | E-mail         |              | X              |
| Facebook identita         | Text          |              | X              |
| Jméno                | Text          |              | X              |
| Celé jméno                 | Text          |              | X              |
| Rod                    | Sada možností    |              | X              |
| Generování                | Text          |              | X              |
| Je povolen e-mail kontaktu  | Dvě možnosti   |              | X              |
| Je povolen telefon kontaktu  | Dvě možnosti   |              | X              |
| Příjmení                 | Text          |              | X              |
| LinkedIn identita         | Text          |              | X              |
| Manažer                   | Vyhledávání        |              | X              |
| Druhé jméno               | Text          |              | X              |
| Mobilní telefon              | Telefon         |              | X              |
| Office Graph identifikátor   | Text          |              | X              |
| Primární e-mailová adresa     | E-mail         |              | X              |
| Primární telefon         | Telefon         |              | X              |
| Povolání                | Text          |              | X              |
| Sociální síť 1          | Sada možností    |              | X              |
| Sociální síť 2          | Sada možností    |              | X              |
| Identita sociální sítě 1 | Text          |              | X              |
| Identita sociální sítě 2 | Text          |              | X              |
| Zdroj                    | Sada možností    | X            | X              |
| Stav                    | Sada možností    | X            | X              |
| Telefon 1               | Telefon         |              | X              |
| Telefon 2               | Telefon         |              | X              |
| Telefon 3               | Telefon         |              | X              |
| Identita Twitteru          | Text          |              | X              |
| Uživatel                      | Vyhledávání        |              | X              |
| Adresa URL webu               | Adresa URL           |              | X              |
| Počet pracovníků             | Text          | X            | X              |
| Typ pracovníka               | Sada možností    | X            | X              |
| Jméno Yomi           | Text          |              | X              |
| Celé jméno Yomi            | Text          |              | X              |
| Příjmení Yomi            | Text          |              | X              |
| Druhé jméno Yomi          | Text          |              | X              |


**Adresa pracovníka**

| **Pole**           | **Datový typ**  | **Požadováno** | **Lze prohledávat** |
|----------------------|----------------|--------------|----------------|
| Číslo v adrese       | Text           | X            | X              |
| Typ adresy         | Sada možností     | X            | X              |
| Město                 | Text           |              | X              |
| Země nebo oblast    | Text           |              | X              |
| Okres               | Text           |              | X              |
| Fax                  | Telefon          |              | X              |
| Je upřednostňovaný         | Dvě možnosti    |              | X              |
| Zeměpisná šířka             | Desetinné číslo |              | X              |
| Řádek 1               | Text           |              | X              |
| Řádek 2               | Text           |              | X              |
| Řádek 3               | Text           |              | X              |
| Zeměpisná délka            | Desetinné číslo |              | X              |
| PSČ          | Text           |              | X              |
| Poštovní schránka      | Text           |              | X              |
| Kód způsobu expedice | Celé číslo   |              | X              |
| Stát nebo provincie    | Text           |              | X              |
| Telefon 1          | Telefon          |              | X              |
| Telefon 2          | Telefon          |              | X              |
| Telefon 3          | Telefon          |              | X              |
| Zóna UPS             | Text           |              | X              |
| Protiúčet UTC           | Celé číslo   |              | X              |
| Pracovní podproces               | Vyhledávání         | X            | X              |


**Osobní údaj pracovníka**

| Pole                             | Datový typ    | Povinné | Lze prohledávat |
|------------------------------------|--------------|----------|------------|
| Město narození                         | Text         |          | X          |
| Země nebo oblast narození            | Sada možností   |          | X          |
| Datum narození                          | Pouze datum    |          | X          |
| Země/region státního občanství      | Sada možností   |          | X          |
| Datum úmrtí                      | Pouze datum    |          | X          |
| Datum ověření stavu invalidního veterána | Pouze datum    |          | X          |
| Vzdělání                          | Text         |          | X          |
| Etnický původ                     | Vyhledávání       |          | X          |
| ExpatriateEndDate                  | Pouze datum    |          | X          |
| ExpatriateStartDate                | Pouze datum    |          | X          |
| Země nebo oblast narození otce     | Sada možností   |          | X          |
| Rod                             | Sada možností   |          | X          |
| Je zakázaný                        | Dvě možnosti  |          | X          |
| Je válečný invalida                | Dvě možnosti  |          | X          |
| Platí daňová výjimka pro zahraniční pracovníky    | Dvě možnosti  |          | X          |
| Je student řádného denního studia               | Dvě možnosti  |          | X          |
| Rodinný stav                     | Sada možností   |          | X          |
| Datum odchodu z vojenské služby          | Pouze datum    |          | X          |
| Datum nástupu vojenské služby        | Pouze datum    |          | X          |
| Země nebo oblast narození matky     | Sada možností   |          | X          |
| Země nebo oblast národnosti      | Sada možností   |          | X          |
| Mateřský jazyk                    | Vyhledávání       |          | X          |
| Počet závislých osob               | Celé číslo |          |            |
| Stav veterána                     | Vyhledávání       |          | X          |
| Pracovní podproces                             | Vyhledávání       | X        | X          |
| Podrobné osobní číslo pracovníka      | Text         | X        | X          |


**Bankovní účet pracovníka**

| **Pole**                 | **Datový typ** | **Požadováno** | **Lze prohledávat** |
|----------------------------|---------------|--------------|----------------|
| Držitel účtu             | Text          |              | X              |
| Identifikace účtu     | Text          |              | X              |
| Popis adresy        | Text          |              | X              |
| Typ bankovního účtu          | Sada možností    |              | X              |
| Kód místa banky         | Text          |              | X              |
| Název pobočky                | Text          |              | X              |
| Číslo pobočky              | Text          |              | X              |
| Město                       | Text          |              | X              |
| Země nebo oblast          | Text          |              | X              |
| Okres                     | Text          |              | X              |
| Popis                | Text          |              | X              |
| Název oblasti              | Text          |              | X              |
| E-mail                      | Text          |              | X              |
| Linka                  | Text          |              | X              |
| Fax                        | Text          |              | X              |
| IBAN                       | Text          |              | X              |
| Řádek 1                     | Text          |              | X              |
| Řádek 2                     | Text          |              | X              |
| Řádek 3                     | Text          |              | X              |
| Mobilní telefon               | Text          |              | X              |
| Jméno osoby             | Text          |              | X              |
| PSČ                | Text          |              | X              |
| Poštovní schránka            | Text          |              |                |
| Směrový kód             | Text          |              | X              |
| Typ směrového kódu banky        | Sada možností    |              | X              |
| Stát nebo provincie          | Text          |              | X              |
| Kód SWIFT                 | Text          |              | X              |
| Telefon                  | Text          |              | X              |
| Číslo telexu               | Text          |              | X              |
| Adresa URL webu                | Text          |              | X              |
| Pracovní podproces                     | Vyhledávání        | X            | X              |
| Číslo bankovního účtu pracovníka | Text          |              | X              |
| Číslo bankovního účtu pracovníka | Text          | X            | X              |

**Fixní kompenzace pracovníka**

| Pole                                | Datový typ      | Povinné | Lze prohledávat |
|---------------------------------------|----------------|----------|------------|
| Společnost                               | Vyhledávání         | X        | X          |
| Typ kompenzace                     | Sada možností     |          | X          |
| Měna                              | Vyhledávání         |          | X          |
| Datum platnosti                        | Pouze datum      |          | X          |
| Událost                                 | Vyhledávání         | X        | X          |
| Směnný kurz                         | Desetinné číslo |          | X          |
| Datum vypršení platnosti                       | Pouze datum      |          | X          |
| Číslo řádku                           | Desetinné číslo |          | X          |
| Interval plateb                         | Vyhledávání         | X        | X          |
| Mzdová sazba                              | Měna       |          | X          |
| Mzdová sazba (základní)                       | Měna       |          | X          |
| Plán                                  | Vyhledávání         | X        | X          |
| Pozice                              | Vyhledávání         | X        | X          |
| Typ procesu                          | Sada možností     | X        | X          |
| Řádek nastavení referenčních bodů            | Vyhledávání         |          | X          |
| Pracovní podproces                                | Vyhledávání         | X        | X          |
| Číslo fixního plánu kompenzace pracovníka      | Text           | X        | X          |

**Osobní identifikační číslo pracovníka**

| Pole                 | Datový typ   | Povinné | Lze prohledávat |
|------------------------|-------------|----------|------------|
| Popis            | Text        |          | X          |
| Typ položky             | Text        |          | X          |
| Datum vypršení platnosti        | Pouze datum   |          | X          |
| Identifikační číslo  | Text        | X        | X          |
| Typ identifikace    | Vyhledávání      | X        | X          |
| Je primární             | Dvě možnosti |          | X          |
| Datum vydání             | Pouze datum   |          | X          |
| Vydávající úřad         | Vyhledávání      | X        | X          |
| Pracovní podproces                 | Vyhledávání      | X        | X          |


## <a name="position-entities"></a>Entity pozice

**Pracovní pozice**

| **Pole**               | **Datový typ**  | **Požadováno** | **Lze prohledávat** |
|--------------------------|----------------|--------------|----------------|
| Aktivace               | Datum a čas  |              | X              |
| K dispozici pro přiřazení | Datum a čas  |              | X              |
| Oddělení               | Vyhledávání         |              | X              |
| Popis              | Text           |              | X              |
| Ekvivalent plného úvazku     | Desetinné číslo |              | X              |
| Pozice                      | Vyhledávání         | X            | X              |
| Číslo pracovní pozice      | Text           | X            | X              |
| Nadřazená pozice úlohy      | Vyhledávání         |              | X              |
| Typ pozice            | Vyhledávání         |              | X              |
| Důchod               | Datum a čas  |              | X              |
| Titul                    | Sada možností     |              | X              |
| Platné od               | Datum a čas  | X            | X              |
| Platné do                 | Datum a čas  |              | X              |


**Typ pozice**

| **Pole**         | **Datový typ** | **Požadováno** | **Lze prohledávat** |
|--------------------|---------------|--------------|----------------|
| Klasifikace     | Sada možností    |              | X              |
| Popis        | Text          |              | X              |
| Název typu pozice | Text          | X            | X              |


**Přiřazení pracovníka k pozici**

| **Pole**                        | **Datový typ** | **Požadováno** | **Lze prohledávat** |
|-----------------------------------|---------------|--------------|----------------|
| Pracovní pozice                      | Vyhledávání        | X            | X              |
| Akce přiřazení pozice pracovníka | Text          | X            | X              |
| Platné od                        | Text          | X            | X              |
| Platné do                          |               |              | X              |
| Pracovní podproces                            |               | X            | X              |

## <a name="job-entities"></a>Pracovní entity

**Práce**

| **Pole**                   | **Datový typ**  | **Požadováno** | **Lze prohledávat** |
|------------------------------|----------------|--------------|----------------|
| Povolit neomezené pozice    | Dvě možnosti    |              | X              |
| Výchozí ekvivalent plného úvazku | Desetinné číslo |              | X              |
| Popis                  | Text           |              | X              |
| Popis práce              | Text           |              | X              |
| Pracovní funkce                 | Vyhledávání         |              | X              |
| Typ práce                     | Vyhledávání         |              | X              |
| Maximální počet pozic  | Celé číslo   |              | X              |
| Název                         | Text           | X            | X              |
| Titul                        | Sada možností     |              | X              |
| Platné od                   | Datum a čas  | X            | X              |
| Platné do                     | Datum a čas  |              | X              |


**Pracovní funkce**

| **Pole**        | **Datový typ** | **Požadováno** | **Lze prohledávat** |
|-------------------|---------------|--------------|----------------|
| Popis       | Text          | X            | X              |
| Název pracovní funkce | Text          | X            | X              |


**Typ úlohy**

| **Pole**    | **Datový typ** | **Požadováno** | **Lze prohledávat** |
|---------------|---------------|--------------|----------------|
| Popis   | Text          | X            | X              |
| Stav osvobození od daně | Sada možností    | X            | X              |
| Název typu práce | Text          | X            | X              |

## <a name="leave-and-absence-entities"></a>Entity pracovního volna a absence

**Opustit registraci**

| **Pole**            | **Datový typ** | **Požadováno** | **Lze prohledávat** |
|-----------------------|---------------|--------------|----------------|
| Základní datum časového rozlišení    | Pouze datum     | X            | X              |
| Časově rozlišené datum zahájení    | Pouze datum     | X            | X              |
| Vlastní datum           | Pouze datum     | X            | X              |
| Má pozastaveno časové rozlišení  | Dvě možnosti   |              | X              |
| LeaveEnrollmentNumber | Text          | X            | X              |
| Plán pracovního volna            | Vyhledávání        | X            | X              |
| Počáteční datum            | Pouze datum     | X            | X              |
| Základní vrstva            | Sada možností    | X            | X              |
| Pracovní podproces                | Vyhledávání        | X            | X              |


**Opustit bankovní transakci**

| **Pole**                    | **Datový typ**  | **Požadováno** | **Lze prohledávat** |
|-------------------------------|----------------|--------------|----------------|
| Množství                        | Desetinné číslo | X            | X              |
| Společnost                       | Vyhledávání         | X            | X              |
| Číslo bankovního účtu dovolené | Text           | X            | X              |
| Plán pracovního volna                    | Vyhledávání         |              | X              |
| Typ pracovního volna                    | Vyhledávání         | X            | X              |
| Datum transakce              | Pouze datum      | X            | X              |
| Číslo transakce            | Desetinné číslo | X            | X              |
| Typ transakce              | Sada možností     | X            | X              |
| Pracovní podproces                        | Vyhledávání         | X            | X              |


**Plán pracovního volna**

| **Pole**        | **Datový typ** | **Požadováno** | **Lze prohledávat** |
|-------------------|---------------|--------------|----------------|
| Frekvence časového rozlišení | Sada možností    | X            | X              |
| Společnost           | Vyhledávání        | X            | X              |
| Popis       | Text          |              | X              |
| Typ pracovního volna        | Vyhledávání        | X            | X              |
| Název              | Text          | X            | X              |
| Počáteční datum        | Pouze datum     | X            | X              |


**Žádost o pracovní volno**

| **Pole**           | **Datový typ** | **Požadováno** | **Lze prohledávat** |
|----------------------|---------------|--------------|----------------|
| Komentář              | Text          | X            | X              |
| Společnost              | Vyhledávání        | X            | X              |
| Číslo žádosti o dovolenou | Text          |              | X              |
| Datum požadavku         | Datum a čas | X            | X              |
| Stav               | Sada možností    | X            | X              |
| Pracovní podproces               | Vyhledávání        | X            | X              |


**Podrobnosti o požadavku na dovolenou**

| **Pole**                  | **Datový typ**  | **Požadováno** | **Lze prohledávat** |
|-----------------------------|----------------|--------------|----------------|
| Množství                      | Desetinné číslo | X            | X              |
| Datum pracovního volna                  | Datum a čas  | X            | X              |
| Žádost o pracovní volno               | Vyhledávání         | X            | X              |
| Podrobnosti o požadavku na dovolenou | Text           | X            | X              |
| Typ pracovního volna                  | Vyhledávání         | X            | X              |


**Typ pracovního volna**

| **Pole**      | **Datový typ** | **Požadováno** | **Lze prohledávat** |
|-----------------|---------------|--------------|----------------|
| Společnost         | Vyhledávání        | X            | X              |
| Popis     | Text          |              | X              |
| Kód příjmů    | Vyhledávání        |              | X              |
| Název typu volna | Text          | X            | X              |


**Pracovní kalendář**

| **Pole**  | **Datový typ** | **Požadováno** | **Lze prohledávat** |
|-------------|---------------|--------------|----------------|
| Společnost     | Vyhledávání        | X            | X              |
| Popis | Text          |              | X              |
| Název        | Text          | X            | X              |


**Datum pracovního kalendáře**

| **Pole**               | **Datový typ** | **Požadováno** | **Lze prohledávat** |
|--------------------------|---------------|--------------|----------------|
| Datum kalendáře            | Pouze datum     | X            | X              |
| Společnost                  | Vyhledávání        |              | X              |
| Stav                   | Text          |              | X              |
| Pracovní kalendář            | Vyhledávání        | X            | X              |
| Datum pracovního kalendáře | Text          | X            | X              |


**Svátek pracovního kalendáře**

| **Pole**  | **Datový typ** | **Požadováno** | **Lze prohledávat** |
|-------------|---------------|--------------|----------------|
| Název        | Text          |              | X              |
| Popis | Text          | X            | X              |


**Řádek data pracovního kalendáře**

| **Pole**                        | **Datový typ** | **Požadováno** | **Lze prohledávat** |
|-----------------------------------|---------------|--------------|----------------|
| Datum svátku                      | Pouze datum     | X            | X              |
| Název                              | Text          |              | X              |
| Svátek pracovního kalendáře             | Vyhledávání        | X            | X              |
| Řádek data pracovního kalendáře | Text          | X            | X              |


**Časový interval pracovního kalenáře**

| **Pole**                         | **Datový typ** | **Požadováno** | **Lze prohledávat** |
|------------------------------------|---------------|--------------|----------------|
| Společnost                            | Vyhledávání        |              | X              |
| Čas ukončení                           | Celé číslo  |              | X              |
| Čas zahájení                         | Celé číslo  |              | X              |
| Pracovní kalendář                      | Vyhledávání        | X            | X              |
| Datum pracovního kalendáře                  | Vyhledávání        | X            | X              |
| Časový interval pracovního kalenáře | Text          | X            | X              |

## <a name="organization-entities"></a>Entity organizace

**Company (Společnost)**

| **Pole**   | **Datový typ** | **Požadováno** | **Lze prohledávat** |
|--------------|---------------|--------------|----------------|
| Kód společnosti | Text          | X            | X              |
| Název         | Text          | X            | X              |


**Oddělení**

| **Pole**        | **Datový typ** | **Požadováno** | **Lze prohledávat** |
|-------------------|---------------|--------------|----------------|
| Číslo oddělení | Text          | X            | X              |
| Popis       | Text          |              | X              |
| Název              | Text          | X            | X              |
| Nadřazené oddělení | Vyhledávání        |              | X              |


**Měna**

| **Pole**         | **Datový typ**  | **Požadováno** | **Lze prohledávat** |
|--------------------|----------------|--------------|----------------|
| Kód měny      | Text           | X            | X              |
| Název měny      | Text           | X            | X              |
| Přesnost měny | Celé číslo   | X            | X              |
| Symbol měny    | Text           | X            | X              |
| Obrázek entity       | Obrázek          |              |                |
| Směnný kurz      | Desetinné číslo | X            | X              |
| Organizace       | Vyhledávání         | X            | X              |
| Stav             | Sada možností     |              | X              |

## <a name="payroll-entities"></a>Entita mzdy

**Platební cyklus**

| **Pole**  | **Datový typ** | **Požadováno** | **Lze prohledávat** |
|-------------|---------------|--------------|----------------|
| Popis | Text          | X            | X              |
| Četnost   | Sada možností    | X            | X              |
| Název        | Text          | X            | X              |


**Mzdové období**

| **Pole**           | **Datový typ** | **Požadováno** | **Lze prohledávat** |
|----------------------|---------------|--------------|----------------|
| Výchozí datum platby | Pouze datum     |              | X              |
| Popis          | Text          |              | X              |
| Platební cyklus            | Vyhledat          | X            | X              |
| Číslo daňového období    | Text          | X            | X              |
| Koncové datum období      | Pouze datum     | X            | X              |
| Počáteční datum období    | Pouze datum     | X            | X              |
| Stav               | Sada možností    |              | X              |


**Kód příjmů mzdy**

| **Pole**              | **Datový typ** | **Požadováno** | **Lze prohledávat** |
|-------------------------|---------------|--------------|----------------|
| Popis             | Text          | X            | X              |
| Zahrnout do typu cyklu plateb | Sada možností    | X            | X              |
| Je produktivní           | Dvě možnosti   | X            | X              |
| Název                    | Text          |              | X              |
| Jednotkové množství           | Sada možností    |              | X              |
| Sledovat FMLA hodiny        | Dvě možnosti   |              | X              |


**Daňová oblast**

| **Pole**        | **Datový typ** | **Požadováno** | **Lze prohledávat** |
|-------------------|---------------|--------------|----------------|
| Město              | Text          |              | X              |
| Země nebo oblast | Text          |              | X              |
| Okres            | Text          |              | X              |
| Název              | Text          | X            | X              |
| Stát nebo provincie | Text          |              | X              |


**Platební období – interval provádění výpočtu zaměstnaneckých výhod**

| **Pole**                                      | **Datový typ** | **Požadováno** | **Lze prohledávat** |
|-------------------------------------------------|---------------|--------------|----------------|
| Interval provádění výpočtu zaměstnaneckých výhod                   | Vyhledávání        | X            | X              |
| Platební období – interval provádění výpočtu zaměstnaneckých výhod | Text          | X            | X              |
| Mzdové období                                      | Vyhledávání        | X            | X              |


**Úhrada na bankovní účet**

| **Pole**                       | **Datový typ**  | **Požadováno** | **Lze prohledávat** |
|----------------------------------|----------------|--------------|----------------|
| Množství                           | Měna       |              | X              |
| Částka (základ)                    | Měna       |              | X              |
| Bankovní účet                     | Vyhledávání         | X            | X              |
| Číslo úhrady na bankovní účet | Text           | X            | X              |
| Společnost                          | Vyhledávání         | X            | X              |
| Měna                         | Vyhledávání         |              | X              |
| Směnný kurz                    | Desetinné číslo |              | X              |
| Je zůstatek                     | Dvě možnosti    |              | X              |
| Priorita                          | Celé číslo   |              | X              |

**Subjekt vydávající identifikaci osob**

| **Pole**           | **Datový typ** | **Požadováno** | **Lze prohledávat** |
|----------------------|---------------|--------------|----------------|
| Popis adresy  | Text          |              | X              |
| Řádek adresy 1       | Text          |              | X              |
| Řádek adresy 2       | Text          |              | X              |
| Řádek adresy 3       | Text          |              | X              |
| Město                 | Text          |              | X              |
| Země nebo oblast    | Sada možností    |              | X              |
| Okres               | Text          |              | X              |
| Popis          | Text          |              | X              |
| E-mail                | Text          |              | X              |
| Linka            | Text          |              | X              |
| Fax                  | Text          |              | X              |
| Název vydávajícího úřadu  | Text          | X            | X              |
| Mobilní telefon         | Text          |              | X              |
| Stránka                 | Text          |              | X              |
| PSČ          | Text          |              | X              |
| Poštovní schránka      | Text          |              | X              |
| SMS                  | Text          |              | X              |
| Stát nebo provincie    | Text          |              | X              |
| Telefon            | Text          |              | X              |
| Telex                | Text          |              | X              |
| Adresa URL webu          | Text          |              | X              |

**Typ osobní identifikace pracovníka**

| **Pole**                        | **Datový typ**  | **Požadováno** | **Lze prohledávat** |
|-----------------------------------|----------------|--------------|----------------|
| Povolené hodnoty                    | Sada možností     |              | X              |
| Země nebo oblast                 | Text           |              | X              |
| Popis                       | Text           |              | X              |
| Pevná délka                      | Celé číslo   |              | X              |
| Formát identifikačního čísla      | Text           |              | X              |
| Typ                              | Sada možností     |              | X              |
| Typ osobní identifikace pracovníka | Text           | X            | X              |

## <a name="fixed-compensation-entities"></a>Entity fixní kompenzace

**Plán fixní kompenzace**

| **Pole**                  | **Datový typ** | **Požadováno** | **Lze prohledávat** |
|-----------------------------|---------------|--------------|----------------|
| Společnost                     | Vyhledávání        | X            | X              |
| Mřížka kompenzace           | Vyhledávání        |              | X              |
| Měna                    | Vyhledávání        | X            | X              |
| Popis                 | Text          | X            | X              |
| Datum platnosti              | Pouze datum     | X            | X              |
| Datum vypršení platnosti             | Pouze datum     | X            | X              |
| Pravidlo zařazení                   | Sada možností    | X            | X              |
| Název                        | Text          | X            | X              |
| Tolerance mimo rozsah      | Sada možností    | X            | X              |
| Interval plateb               | Vyhledávání        | X            | X              |
| Doporučení povoleno      | Dvě možnosti   | X            | X              |
| Nastavení řádku referenčního bodu  | Vyhledávání        |              | X              |
| Typ                        | Sada možností    | X            | X              |

**Kompenzační mřížka**

| **Pole**                  | **Datový typ** | **Požadováno** | **Lze prohledávat** |
|-----------------------------|---------------|--------------|----------------|
| Společnost                     | Vyhledávání        | X            | X              |
| Měna                    | Vyhledávání        |              | X              |
| Popis                 | Text          | X            | X              |
| Datum platnosti              | Pouze datum     |              | X              |
| Datum vypršení platnosti             | Pouze datum     |              | X              |
| Název                        | Text          | X            | X              |
| Nastavení referenčního bodu       | Vyhledávání        | X            | X              |
| Typ                        | Sada možností    | X            | X              |

**Úroveň kompenzace**

| **Pole**      | **Datový typ** | **Požadováno** | **Lze prohledávat** |
|-----------------|---------------|--------------|----------------|
| Popis     | Text          |              | X              |
| Název            | Text          | X            | X              |
| Typ            | Sada možností     | X            | X              |

**Interval plateb kompenzace**

| **Pole**                  | **Datový typ**   | **Požadováno** | **Lze prohledávat** |
|-----------------------------|-----------------|--------------|----------------|
| Faktor ručního přepočtu    | Desetinné číslo  |              | X              |
| Společnost                     | Vyhledávání          | X            | X              |
| Popis                 | Text            |              | X              |
| Faktor hodinového přepočtu    | Desetinné číslo  |              | X              |
| Měsíční koeficient převodu   | Desetinné číslo  |              | X              |
| Název                        | Text            | X            | X              |
| Období                      | Sada možností      |              | X              |
| Týdenní koeficient převodu    | Sada možností      |              | X              |


**Nastavení referenčního bodu kompenzace**

| **Pole**          | **Datový typ**   | **Požadováno** | **Lze prohledávat** |
|---------------------|-----------------|--------------|----------------|
| Společnost             | Vyhledávání          | X            | X              |
| Typ kompenzace   | Sada možností      | X            | X              |
| Popis         | Text            | X            | X              |
| Název                | Text            | X            | X              |

**Linie nastavení referenčního bodu kompenzace**

| **Pole**            | **Datový typ**   | **Požadováno** | **Lze prohledávat** |
|-----------------------|-----------------|--------------|----------------|
| Společnost               | Vyhledávání          | X            | X              |
| Popis           | Text            | X            | X              |
| Číslo řádku           | Desetinné číslo  | X            | X              |
| Název                  | Text            | X            | X              |
| Nastavení referenčního bodu | Vyhledávání          | X            | X              |

**Oblast kompenzace**

| **Pole**      | **Datový typ** | **Požadováno** | **Lze prohledávat** |
|-----------------|---------------|--------------|----------------|
| Popis     | Text          | X            | X              |
| Název            | Text          | X            | X              |

**Struktura kompenzací**

| **Pole**                    | **Datový typ**   | **Požadováno** | **Lze prohledávat** |
|-------------------------------|---------------  |--------------|----------------|
| Množství                        | Měna        |              | X              |
| Základní částka                   | Měna        |              | X              |
| Společnost                       | Vyhledávání          | X            | X              |
| Číslo struktury kompenzací | Text            | X            | X              |
| Měna                      | Vyhledávání          |              | X              |
| Směnný kurz                 | Desetinné číslo  |              | X              |
| Mřížka                          | Vyhledávání          | X            | X              |
| Úroveň                         | Vyhledávání          | X            | X              |
| Referenční bod               | Vyhledávání          | X            | X              |
| Nastavení řádku referenčního bodu    | Vyhledávání          | X            | X              |

**Událost fixní kompenzace**

| **Pole**            | **Datový typ**   | **Požadováno** | **Lze prohledávat** |
|-----------------------|-----------------|--------------|----------------|
| Společnost               | Vyhledávání          | X            | X              |
| Popis           | Text            | X            | X              |
| Typ události            | Sada možností      | X            | X              |
| Je aktivní             | Dvě možnosti     | X            |                |
| Název                  | Text            | X            | X              |

## <a name="entity-relationship-models"></a>Modely vztahu entity

### <a name="worker"></a>Pracovní podproces
![Pracovní podproces](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>Práce a pracovní pozice
![Práce a pracovní pozice](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>Zaměstnanecké výhody
![Zaměstnanecké výhody](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>Kompenzace
![Kompenzace](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>Odejít
![Odejít](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>Pracovní kalendář
![Pracovní kalendář](./media/HCMCommon-work-calendar-entity-diagram.png)
