---
title: "Definování komunikace v maloobchodní síti (Commerce Data Exchange)"
description: "V tomto článku je přehled služby Commerce Data Exchange a jejích součástí. Tento článek vysvětluje části hraje každou komponentu v přenosu dat mezi Microsoft Dynamics 365 pro operace a maloobchodní sítě."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27021
ms.assetid: 179b1629-ac90-4cfb-b46a-5bda56c4f451
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 29938d962db42a521dd8dc03b8e45e0e34410e4d
ms.openlocfilehash: d3b36ec2a3f859215d93dd7ebf1f1ecfb2731c59
ms.lasthandoff: 03/31/2017


---

# <a name="define-retail-channel-communications-commerce-data-exchange"></a>Definování komunikace v maloobchodní síti (Commerce Data Exchange)

[!include[banner](../includes/banner.md)]


V tomto článku je přehled služby Commerce Data Exchange a jejích součástí. Tento článek vysvětluje části hraje každou komponentu v přenosu dat mezi Microsoft Dynamics 365 pro operace a maloobchodní sítě.

<a name="overview"></a>Přehled
--------

Commerce Data Exchange je systém, který přenáší data mezi Dynamics 365 pro operace a maloobchodní sítě, například online obchody nebo cihel a Malty obchody. Databáze, která ukládá data pro maloobchodní sítě se liší od 365 Dynamics pro operace databáze. Databáze kanálů obsahuje pouze data, která jsou nutná pro maloobchodní transakce. Hlavní data v 365 Dynamics pro operace a je distribuována do kanálů. Transakční data je vytvořen v tomto systému prodeje (POS) nebo online úložiště a poté odeslány do 365 Dynamics pro operace. Distribuce dat je asynchronní. Jinak řečeno proces shromažďování a balení dat ve zdroji probíhá odděleně od procesu přijetí a použití dat v cíli. Pro některé situace, například vyhledávání ceny a zásob, musí být data načtena v reálném čase. Pro podporu scénářů, Commerce Data Exchange je také služba, která umožňuje komunikaci v reálném čase mezi Dynamics 365 pro operace a kanál. 

[![Aktualizovat obrázek maloobchodní](./media/updated-retail-graphic.png)](./media/updated-retail-graphic.png)  

## <a name="async-service"></a>Asynchronní služba
Sledování na 365 Dynamics pro operace databáze změn Microsoft SQL Server slouží k určení data změny, které musí být zaslány do kanálů. Na základě distribučního plánu, 365 Dynamics pro operace balíčky data a uloží jej do centrálního úložiště (úložiště objektů blob Azure). Samostatný dávkový proces používá knihovnu Commerce Data Exchange: Async Client ke vložení tohoto balíčku dat do databáze kanálu. 

[![Async Service](./media/async-300x239.png)](./media/async.png)

### <a name="retail-scheduler"></a>Maloobchodní plánovač

Úlohy plánovače jsou mechanismem pro distribuci dat do skladových míst a z nich. Úlohy jsou tvořeny dílčími úlohami, které určují tabulky a pole tabulky obsahující data, která mají být distribuována. Dynamics 365 pro operace zahrnuje předdefinované Plánovač úlohy a dílčí úlohy replikace požadavků většiny organizací. Jsou vytvořeny následující typy předem definovaných úloh:

-   **Úlohy stahování** – ke stažení úlohy odeslání dat, která se změnila od 365 Dynamics pro provoz databází kanálu. Úpravy záznamů jsou sledovány prostřednictvím sledování změn systému SQL Server.
-   **Odeslat úlohy (úlohy P)** – vyžádané úlohy odeslání prodejní transakce z kanálu do 365 Dynamics pro operace databáze. Úlohy P odesílají data postupně. Při spuštění úlohy P knihovna klienta Async Client zkontroluje počítadlo replikace pro záznamy, které již byly přijaty z umístění. Záznam je odeslán pouze v případě, že počítadlo replikace je vyšší než nejvyšší zjištěná hodnota. Úlohy P neaktualizují data, která již byla odeslána.

Plán distribuce se používá ke spuštění přenosu dat ručně nebo pomocí plánování dávkové úlohy v 365 Dynamics pro operace. Plán distribuce může obsahovat jednu nebo více skupin dat kanálu a jednu nebo více úloh plánovače.

## <a name="realtime-service"></a>Služba v reálném čase
Commerce Data Exchange: Real-time Service je integrovaná služba, která poskytuje komunikaci v reálném čase mezi Dynamics 365 pro operace a maloobchodní sítě. Služba v reálném čase umožňuje jednotlivé počítače POS a online obchodů můžete načíst konkrétní data z 365 Dynamics pro operace v reálném čase. Ačkoli většina klíče operace mohou být provedeny v databázi místních kanálů, následující scénáře vyžadují přímý přístup k datům, která je uložena v 365 Dynamics pro operace:

-   Vydání a uplatnění dárkových poukazů.
-   Uplatnění věrnostních bodů.
-   Vydání a uplatnění dobropisů.
-   Vytvoření a aktualizace záznamů odběratele.
-   Vytvoření, aktualizace a dokončení prodejních objednávek.
-   Přijetí zásob v porovnání s nákupní objednávkou nebo převodním příkazem.
-   Provedení inventury.
-   Získání prodejních transakcí mezi obchody a dokončení transakce vrácení.

[![Real-time Service](./media/rts.png)](./media/rts.png) 

Předdefinovaný profil služby Real-time Service je vytvořen.




