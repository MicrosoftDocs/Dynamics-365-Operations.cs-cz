---
title: "Definování komunikace v maloobchodní síti (Commerce Data Exchange)"
description: "V tomto článku je přehled služby Commerce Data Exchange a jejích součástí. Vysvětluje roli každé součásti, kterou hraje při přenosu dat mezi aplikací Microsoft Dynamics 365 for Operations a maloobchodní sítí."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
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


V tomto článku je přehled služby Commerce Data Exchange a jejích součástí. Vysvětluje roli každé součásti, kterou hraje při přenosu dat mezi aplikací Microsoft Dynamics 365 for Operations a maloobchodní sítí.

<a name="overview"></a>Přehled
--------

Commerce Data Exchange je systém, který přenáší data mezi aplikací Microsoft Dynamics 365 for Operations a maloobchodními kanály, jako jsou například online obchody nebo kamenné obchody. Databáze obsahující data pro maloobchodní sítě se liší od databáze Microsoft Dynamics 365 for Operations. Databáze kanálů obsahuje pouze data, která jsou nutná pro maloobchodní transakce. Hlavní data jsou konfigurována v aplikaci Microsoft Dynamics 365 for Operations a distribuována do kanálů. Transakční data jsou vytvořena v systému pokladních míst (POS) nebo online obchodě a poté odeslána do aplikace Dynamics 365 for Operations. Distribuce dat je asynchronní. Jinak řečeno proces shromažďování a balení dat ve zdroji probíhá odděleně od procesu přijetí a použití dat v cíli. Pro některé situace, například vyhledávání ceny a zásob, musí být data načtena v reálném čase. Aby bylo možné tyto situace podporovat, Commerce Data Exchange zahrnuje také službu, která umožňuje komunikaci v reálném čase mezi aplikací Dynamics 365 for Operations a kanálem. 

[![Aktualizovaná grafika maloobchodu](./media/updated-retail-graphic.png)](./media/updated-retail-graphic.png)  

## <a name="async-service"></a>Asynchronní služba
Sledování změn na serveru Microsoft SQL Server v databázi aplikace Dynamics 365 for Operations slouží k určení změn dat, která musí být odeslána do kanálů. Na základě plánu distribuce aplikace Dynamics 365 for Operations zabalí tato data a uloží je do centrálního úložiště (úložiště objektů blob Azure). Samostatný dávkový proces používá knihovnu Commerce Data Exchange: Async Client ke vložení tohoto balíčku dat do databáze kanálu. 

[![Asynchronní služba](./media/async-300x239.png)](./media/async.png)

### <a name="retail-scheduler"></a>Maloobchodní plánovač

Úlohy plánovače jsou mechanismem pro distribuci dat do skladových míst a z nich. Úlohy jsou tvořeny dílčími úlohami, které určují tabulky a pole tabulky obsahující data, která mají být distribuována. Dynamics 365 for Operations obsahuje předdefinované úlohy plánovače a dílčí úlohy, které vyhovují požadavkům většiny organizací na replikaci. Jsou vytvořeny následující typy předem definovaných úloh:

-   **Stáhnout úlohy** – Stažené úlohy odesílají data, která se změnila z aplikace Dynamics 365 for Operations na databáze kanálů. Úpravy záznamů jsou sledovány prostřednictvím sledování změn systému SQL Server.
-   **Odeslat úlohy (úlohy P)** – Odeslání úloh vyžádá prodejní transakce z kanálu do databáze aplikace Dynamics 365 for Operations. Úlohy P odesílají data postupně. Při spuštění úlohy P knihovna klienta Async Client zkontroluje počítadlo replikace pro záznamy, které již byly přijaty z umístění. Záznam je odeslán pouze v případě, že počítadlo replikace je vyšší než nejvyšší zjištěná hodnota. Úlohy P neaktualizují data, která již byla odeslána.

Plán distribuce slouží ke spuštění převodu dat ručně nebo prostřednictvím naplánování dávkové úlohy v aplikaci Dynamics 365 for Operations, Plán distribuce může obsahovat jednu nebo více skupin dat kanálu a jednu nebo více úloh plánovače.

## <a name="realtime-service"></a>Služba Realtime Service
Commerce Data Exchange: Real-time Service je integrovaná služba, která poskytuje komunikaci v reálném čase mezi aplikací Dynamics 365 for Operations a maloobchodními kanály. Real-time Service umožňuje jednotlivým POS počítačům a online obchodům získat určitá data z aplikace Dynamics 365 for Operations v reálném čase. Přestože většinu klíčových operací lze provádět v místní databázi kanálu, následující scénáře vyžadují přímý přístup k datům, která jsou uložena v aplikaci Dynamics 365 for Operations:

-   Vydání a uplatnění dárkových poukazů.
-   Uplatnění věrnostních bodů.
-   Vydání a uplatnění dobropisů.
-   Vytvoření a aktualizace záznamů odběratele.
-   Vytvoření, aktualizace a dokončení prodejních objednávek.
-   Přijetí zásob v porovnání s nákupní objednávkou nebo převodním příkazem.
-   Provedení inventury.
-   Získání prodejních transakcí mezi obchody a dokončení transakce vrácení.

[![Služba Real-time Service](./media/rts.png)](./media/rts.png) 

Bude vytvořen předem definovaný profil služby Real-time Service.




