---
title: "Nastavení centralizovaných plateb"
description: "Postupujte podle těchto kroků k přípravě zpracování plateb v jedné právnické osobě jménem ostatních právnických osob v organizaci."
author: kweekley
manager: AnnBe
ms.date: 05/09/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62243
ms.assetid: ffd17b5f-9aea-40e0-be49-d8702f615256
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c91d02bfb5e51a7eb34234abb982242bc9f7610f
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-centralized-payments"></a>Nastavení centralizovaných plateb

[!include[banner](../includes/banner.md)]


Postupujte podle těchto kroků k přípravě zpracování plateb v jedné právnické osobě jménem ostatních právnických osob v organizaci. Před zahájením práce je nutné dokončit následující nastavení:

-   Vytvořte právnické osoby.
-   Nastavte obecné parametry hlavní knihy a účtové osnovy.
-   Nastavte parametry závazků a parametry pohledávek (v závislosti na modulech, které používají centralizované platby).
-   Nastavte mezipodnikové účetnictví.

## <a name="set-up-an-organizational-hierarchy-for-centralized-payments"></a>Nastavit organizační hierarchii pro centralizované platby
Musíte nastavit organizační hierarchii pro centralizované platby. Stejná organizační hierarchie slouží také ke zpracování centralizovaných plateb dodavatelů a centralizovaných plateb odběratelů. **Poznámka:** u centralizovaných plateb na struktuře hierarchie nezáleží. Každý právní subjekt v hierarchii bude moci zpracovat platby jménem každého dalšího právního subjektu v hierarchii. Na stránce **Organizační hierarchie** můžete vytvořit novou organizační hierarchii. V poli **Účel** je nutné vybrat **Centralizované platby**. 

## <a name="set-up-an-intercompany-account-for-centralized-payments"></a>Nastavení mezipodnikového účtu pro centralizované platby
Pokud jsou platební transakce u aktuální právnické osoby vyrovnány oproti fakturám u jiných právnických osob, budou pro každou právnickou osobu vytvořeny odpovídající kreditní a debetní transakce. Je nutné zadat právnickou osobu, ve které jsou zaúčtovány odpovídající platební slevy a částky realizovaného zisku nebo ztráty. Před zahájením práce rozhodněte, kterou právnickou osobu budete používat ke zpracování plateb dodavatelů a odběratelů. Jestliže jedna právnická osoba zpracovává platby dodavatelů, ale jiná právnická osoba zpracovává platby odběratelů, budete muset do každé právnické osoby přepínat. Na stránce **Mezipodnikové účetnictví** můžete vybrat záznam mezipodnikového vztahu pro právnickou osobu, jejímž jménem budete zpracovávat platby. 

Na kartě **Centralizované platby dodavatelů** můžete vybrat, zda mají být hotovostní slevy zaúčtovány pro právnickou osobu platby (nebo jiné transakce, která snižuje zůstatek účtu dodavatele) nebo pro společnost faktury (nebo jiné transakce, která zvyšuje zůstatek účtu dodavatele). Tento výběr použijte spolu s polem **Správa platební slevy** na stránkách **Parametry závazků** a **Parametry pohledávek**. Pro tolerance přeplatků a haléřových rozdílů je používáno nastavení právnické osoby platby. Pro tolerance nedoplatků a haléřových rozdílů je používáno nastavení právnické osoby faktury.

## <a name="map-vendor-accounts-across-legal-entities"></a>Mapování účtů dodavatele napříč právnickými osobami
Pokud zašlete dodavateli platbu od jedné právnické osoby a chcete pro něj vybrat faktury u jiných právnických osob, je nutné zajistit, aby všechny odpovídající účty dodavatele používaly u právnických osob stejné ID adresáře. Pokud obdržíte platbu od odběratele, který platí faktury ve více právnických osobách, je nutné zajistit, aby všechny odpovídající účty odběratele používaly u všech právnických osob stejné ID adresáře.

## <a name="set-up-posting-profiles-for-centralized-payments"></a>Nastavení účetních profilů pro centralizované platby
Při vytváření platby u jedné právnické osoby, která slouží k úhradě faktur u jiných právnických osob, se musí ID účetních profilů obou právnických osob shodovat. Chcete-li pomoci zajistit, aby byly platby správně vytvářeny, nastavte u každé právnické osoby faktury účetní profil, který odpovídá účetním profilům používaným u právnických osob platby. Přepněte na první právnickou osobu faktury a poté na stránce **Účetní profil dodavatele** můžete vytvořit nový účetní profil nebo upravit existující účetní profil. Možnosti vybrané pro účetní profil u právnické osoby faktury se nemusí shodovat s nastavením účetního profilu u právnické osoby platby.

## <a name="set-up-methods-of-payment-for-centralized-payments"></a>Nastavení metod platby pro centralizované platby
Při vytváření platby u jedné právnické osoby, která slouží k úhradě faktur u jiných právnických osob, se musí ID způaobu platby obou právnických osob shodovat. Chcete-li pomoci zajistit, aby byly platby správně vytvářeny, nastavte u každé právnické osoby faktury metodu platby, která odpovídá metodám platby používaným u právnické osoby platby. Přepněte na první právnickou osobu faktury a poté na stránce **Metody platby** můžete vytvořit novou metodu platby nebo upravit existující metodu platby. Výběry provedené u metody platby u právnické osoby faktury se nemusejí shodovat s nastavení metody platby u právnické osoby platby.

## <a name="set-up-default-descriptions"></a>Nastavit výchozí popisy
Výchozí popis můžete definovat pro mezipodnikové doklady vyrovnání. Výchozí popis je v průběhu procesu vyrovnání mezi společnostmi zahrnut v transakcích počátečního a koncového data splatnosti. Na stránce **Výchozí popisy** můžete vytvořit nové popisy pro **Mezipodnikové vyrovnání odběratele** i **Mezipodnikové vyrovnání dodavatele** tak, že vyberte jazyk a zadáte text.




