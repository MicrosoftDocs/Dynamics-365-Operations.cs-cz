---
title: "Uživatelské nastavení a nastavení jazyka aplikace POS"
description: "Toto téma popisuje, jak změnit nastavení jazyka v moderní POS maloobchodní (MPOS) a Cloud POS."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: bf5b75572529bb497d3079752de187f30aa59294
ms.lasthandoff: 03/31/2017


---

# <a name="pos-application-and-user-language-settings"></a>Uživatelské nastavení a nastavení jazyka aplikace POS

[!include[banner](includes/banner.md)]


Toto téma popisuje, jak změnit nastavení jazyka v moderní POS maloobchodní (MPOS) a Cloud POS.

<a name="overview"></a>Přehled
========

Moderní POS maloobchodní (MPOS) a Cloud POS podporují kde nastavení jazyka a překlad může být odlišná nastavení úložiště a uživatelského prostředí. Úložiště může například nacházet v oblasti, kde je angličtina nejběžnější pro své zákazníky, ale raději použijte aplikaci s francouzskými překlady některých zaměstnanců.

## <a name="data-language"></a>Jazyk dat
Bez ohledu na nastavení uživatele MPOS a Cloud POS bude vždy používat nastavení jazyka obchodu určit překlady používaných pro data. Tím bude zajištěno, že všichni uživatelé a zákazníci budou mít konzistentní zkušenosti.  Příklady dat:

-   Produkty
-   Atributy a hodnoty
-   Názvy kategorie
-   Tištěné nebo e-mailem odeslané transakční příjmy
-   Názvy způsobu platby
-   Zprávy řádkového displeje

Jazyk obchodu bude použito pro hlavní přihlašovací obrazovce POS, protože uživatel není známo před přihlášením. Pokud překlad není k dispozici pro jazyk obchodu, POS se vrátí do jazyka společnosti.

### <a name="configuring-the-stores-language-setting"></a>Konfigurace nastavení jazyka obchodu

Ve skladovém jazykové nastavení z **všechny maloobchodní obchody** na **maloobchodu** stránky pod ** Obecné &gt;místní nastavení &gt;jazyk. ** Použijte rozevírací dolů zvolit jazyk pro každý obchod.

## <a name="user-interface-language"></a>Jazyk uživatelského rozhraní
Nastavení jazyka uživatele POS určuje překlady používá v uživatelském rozhraní aplikace. Jedná se o popisky, nabídek a seznamů, které nejsou považovány za data. Jedinou výjimkou je text, který je zobrazen na mřížky tlačítek POS. Tlačítko mřížky nepodporují překlady, tak, aby se vždy zobrazovaly text definované na tlačítku. Za účelem podpory přeložený tlačítka, budete muset zkopírovat a udržovat samostatné tlačítko mřížky a přiřadit uživatelům podle potřeby.

### <a name="configuring-the-users-language-setting"></a>Konfigurace nastavení jazyka uživatele

Nastavení jazyka uživatele POS je nastavena z **všechny pracovníky** na **pracovní** stránky pod **maloobchodní &gt;jazyk**.  Na kartě hlavní profil není nastavena.  Toto nastavení nepoužívá POS. Pokud není jazyk uživatele nastaven, nebo pokud je nastaven na jazyk, pro který nejsou k dispozici překlady, POS obnoví používání jazyka obchodu.  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| ** **       | **Jazyk uživatelského rozhraní** ** **      | **Jazyk dat (produkty, formáty příjemky, řádkový displej atd.)** |
| **Company (Společnost)** | Výchozí                    | Výchozí                                                           |
| **Obchod**   | Přepsání společnosti          | Přepsání společnosti                                                 |
| **User**    | Přepsání obchodu nebo společnosti | Nikdy                                                             |






