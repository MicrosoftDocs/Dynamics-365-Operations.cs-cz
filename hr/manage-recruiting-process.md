---
title: "Řízení náborového procesu"
description: "Tento článek popisuje koncept, který náboráři mohou použít pro sledování kroků v procesu náboru, včetně úsilí inzerovat otevřené pozice a provádět nábor uchazečů, sledovat informace v přihlášce a o uchazeči, vést pohovor s uchazeči a vybírat jednoho nebo více uchazečů pro naplnění otevřené pozice ve vaší organizaci."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HRMApplication, HRMRecruitingTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7501
ms.assetid: 1ad725bf-20e2-42a1-8068-111f7ddddad9
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 6f4429202efd0506378d681188035c5cc69f56a1
ms.openlocfilehash: 551e15ed31953d6e5fc99a1177c1310194ea95d0
ms.lasthandoff: 03/31/2017


---

# <a name="manage-a-recruiting-process"></a>Řízení náborového procesu

[!include[banner](includes/banner.md)]


Toto téma popisuje koncepci, náboráře můžete sledovat kroky v procesu náboru, včetně úsilí o otevřené pozice inzerovat a nábor uchazečů, sledování informací o žadateli a aplikace, dotazování uchazečů a výběrem jednoho nebo více zájemců k vyplnění otevřené pozice v organizaci.

<a name="overview"></a>Přehled
--------

Náborové projekty vám mohou pomoci uspořádat kroky, které budete provádět při vyplňování otevřených pozic v právnické osobě. Žadatel je osoba, která platí pro zaměstnanost k rozlehlé síti.  Aplikace je vyjádření žadatele zájem zástupcem společnosti a může být vázána náborového projektu na express zájem o konkrétní otevírací.  Jeden žadatel může mít více aplikací v rámci stejné právnické osobě nebo více společností ve vaší organizaci.

<a name="recruitment-projects"></a>Náborové projekty
--------------------

Náborové projekty umožňují náboráře a sledování průběhu vůči plnění jedné nebo více otevřených položek.  Náborového projektu identifikuje oddělení a úlohy, pro které jsou otevřeny jednu nebo více pozic. Náborové projekty sledují také následující informace pro otevřené pozice:
-   Specifický počet otevřených pozic
-   Personální konzultant a alternativní kontakt pro pozici
-   Datum schválení žádosti
-   Konečný termín přihlášky
-   Odhadované počáteční datum

Náborový projekt obsahuje **Pracovní inzerát** použitý v **Samoobsluze pro zaměstnance** pro inzerování otevřené pozice. Pokud chcete zobrazit otevřenou pozici pro zaměstnance, musí mít náborový projekt **Pracovní inzerát**, pole** Zobrazit v samoobsluze pro zaměstnance** musí být nastaveno na hodnotu Ano, pole **Konečný termín přihlášky** musí být nastaven na budoucí datum a náborový projekt musí mít hodnotu **Stav projektu** Zahájeno. V následující tabulce jsou uvedeny možné náborového projektu stavy a jejich popis.

| **Status**    | **Indicates that…**                                                                  |
|-----------|------------------------------------------------------------------------------------------|
| Plánováno | Úsilí náboru se připravuje.  Nábor ještě nezačalo pro tento projekt. |
| Zahájeno   | Žádosti jsou nyní přijímány pro volná místa v projektu.                    |
| Dokončeno  | Všechna volná místa pro tento projekt byla naplněna.                                          |
| Stornováno  | Nábor pro tento projekt byl zrušen.                                           |

Náboráři mohou zaznamenávat také **Média** použitá pro reklamu volné pozice skrze externí kanály a sledovat **Vývoj** s ohledem na projekt nebo žádost.

<a name="applicants"></a>Uchazeči
----------

Žadatel je osoba, která platí pro úlohy v rozlehlé síti.  Žadatelé jsou sdíleny všechny právnické osoby v organizaci poskytující velký talent pro hledání z fond. Můžete spravovat odkazy, kompetence, požadavky a osobní údaje pro uchazeče. Při vytvoření záznamu žadatele se vytvoří osobní záznam tohoto uchazeče v globálním adresáři. Pomocí stránky **Uchazeč** můžete provádět aktualizace následujících informací pro globální adresář pro osoby, které jsou uchazeči:
-   Informace adresy
-   Kontaktní informace
-   Identifikační informace
-   Podrobnosti o jméně
-   Osobní údaje

## <a name="applications"></a>Aplikace
Na stránce **Přihláška** můžete zaznamenat údaje z přijatých žádosti o zaměstnání. Aplikace je vyjádření žadatele zájem o práci v organizaci.  Chcete-li vytvořit aplikaci, žadatel musí již existovat jako žadatele nebo osoby v systému.
Žádosti o zaměstnání odeslané uchazeči prostřednictvím webu jsou buď vyžádané žádosti, které byly zadány v reakci na pracovní inzerát, nebo nevyžádané žádosti. Vyžádané žádosti jsou automaticky přiřazeny k náborovému projektu, na jehož základě byl vytvořen daný pracovní inzerát. Nevyžádané žádosti jsou přiřazeny k náborovému projektu, který je určen v oblasti **Nábor** na stránce **Parametry lidských zdrojů**.
### <a name="application-status"></a>Stav přihlášky

Stav přihlášky označuje, kde se přihláška nachází v procesu náboru. V následující tabulce jsou uvedeny možné stavy přihlášky a jejich popis.

| Stav    | Udává, že...                                                                           |
|-----------|-------------------------------------------------------------------------------------------|
| Přijato  | Datum, kdy byla přihláška přijata.                                                             |
| Potvrzeno | Uchazečům mohou být odeslána potvrzení o příjmu žádosti.            |
| Pohovor | Pozvánka k pohovoru může být odeslána uchazeči.                                     |
| Zamítnutí | Uchazeči může být odesláno zamítavé vyjádření.                                          |
| Stornováno  | Uchazeči může být odesláno potvrzení odstoupení. Tento status se přiřazuje ručně. |
| Zaměstnán  | Uchazeči může být odeslána nabídka k zaměstnání.                                         |

### <a name="correspondence-actions"></a>Akce korespondence

Korespondenční akce **Přihlášky** určuje šablonu e-mailu nebo dokumentu, která se použije ke komunikaci s uchazečem, který podal přihlášku. Můžete přiřadit **záložky přihlášek** s Korespondenční akce je možné použít hodnoty z aplikace žadatele, rozhovor a náborového projektu stránky v komunikaci s uchazeči.  **Šablony e-mailu aplikace** pro akce korespondence k rychlému odeslání e-mailů žadatelům, kteří mají s určitým stavem a korespondence akce kombinací aplikace nelze vytvořit. Například může odeslat e-mail s potvrzením pro všechny aplikace s **stav** přijato a **akce korespondence** přijato.  Po odeslání e-mailu, máte možnost automaticky aktualizovat stav aplikace.

## <a name="application-routing"></a>Směrování přihlášek

Má-li přihlášku zkontrolovat několik pracovníků, lze pro vytvoření seznamu střídání zaměstnanců pro řízení procesu použít stránku **Směrování přihlášek**.

## <a name="interviews"></a>Pohovory

**Pohovory uchazečů** z lze naplánovat **aplikace** stránky.  Použití **odeslat informace o schůzce** tlačítko Odeslat soubor kalendáře s informací o plánu rozhovor uchazeče a tazatele.

## <a name="skill-mapping"></a>Mapování dovednosti

**Mapování dovedností** a **Profily mapování dovedností** slouží k identifikaci uchazečů, kteří mohou být vhodní pro volnou pozici.

## <a name="hiring-applicants"></a>Přijímání uchazečů

Pomocí stránky **Přihlášky** můžete najmou uchazeče. Při náboru žadatele bude mít záznam přihlášky stav **Zaměstnán** a osobní záznam uchazeče v globálním adresáři je přidružen k novému záznamu pracovníka. Změny informací v globálním adresáři pro nový záznam pracovníka je zobrazen také v záznamu žadatele. To může pomoci snížení objemu zadávaných dat, pokud nového pracovníka stále platí pro různé úlohy v rámci rozlehlé sítě.  Existující pracovní zařazení do nového umístění, klepněte na tlačítko **změnit pozici** v **stav aplikace** drop dolů inicializovat proces přenosu.






