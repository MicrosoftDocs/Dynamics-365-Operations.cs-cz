---
title: "Uživatelské nastavení a nastavení jazyka aplikace POS"
description: "Toto téma popisuje, jak změnit nastavení jazyka v Retail Modern POS (MPOS) a Cloud POS."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
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


Toto téma popisuje, jak změnit nastavení jazyka v Retail Modern POS (MPOS) a Cloud POS.

<a name="overview"></a>Přehled
========

Retail Modern POS (MPOS) a Cloud POS podporují prostředí, kde se může nastavení jazyka a překlady lišit mezi nastavením obchodu a uživatelským nastavením. Obchod se může například nacházet v oblasti, kde zákazníci preferují angličtinu, ale někteří pracovníci dávají přednost používání aplikací s francouzskými překlady.

## <a name="data-language"></a>Jazyk dat
Bez ohledu na uživatelské nastavení bude MPOS a Cloud POS vždy používat nastavení jazyka obchodu k určení překladů používaných pro data. Tím se zajistí, že všichni uživatelé a zákazníci budou mít konzistentní zkušenosti.  Příklady popisů dat:

-   Produkty
-   Atributy a hodnoty
-   Názvy kategorie
-   Tištěné nebo e-mailem odeslané transakční příjmy
-   Názvy způsobu platby
-   Zprávy řádkového displeje

Jazyk obchodu bude použit také pro hlavní přihlašovací obrazovku POS, protože uživatel není znám před přihlášením. Pokud překlad není k dispozici pro jazyk obchodu, POS se vrátí k jazyku společnosti.

### <a name="configuring-the-stores-language-setting"></a>Konfigurace nastavení jazyka obchodu

Jazyko obchodu se nastavuje ve složce **Všechny maloobchody** na stránce **Maloobchod** v části **Obecné &gt; Regionální nastavení &gt; Jazyk. **Pomocí rozevíracího seznamu vyberte jazyk pro každý obchod.

## <a name="user-interface-language"></a>Jazyk uživatelského rozhraní
Nastavení jazyka uživatele POS určuje překlady používané v uživatelském rozhraní aplikace. Jedná se o všechny popisky, nabídky a seznamy, které nejsou považovány za data. Jedinou výjimkou je text, který je zobrazen na tlačítkách mřížky POS. Tlačítka mřížky nepodporují překlady, takže budou vždy zobrazovaly text definovaný na tlačítku. Abyste získali podporu přeložených tlačítek, budete muset zkopírovat a udržovat samostatné mřížky tlačítek a přiřadit je uživatelům podle potřeby.

### <a name="configuring-the-users-language-setting"></a>Konfigurace nastavení jazyka uživatele

Jazyk uživatele POS se nastavuje v okně **Všichni pracovníci** na stránce **Pracovník** pod **Maloobchod &gt; Jazyk**.  Není nastavená na hlavní kartě Profil.  POS toto nastavení nepoužívá. Pokud není jazyk uživatele nastaven, nebo pokud je nastaven na jazyk, pro který nejsou k dispozici překlady, POS obnoví používání jazyka obchodu.  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| ** **       | **Jazyk uživatelského rozhraní** ** **      | **Jazyk dat (produkty, formáty příjemky, řádkový displej atd.)** |
| **Company (Společnost)** | Výchozí                    | Výchozí                                                           |
| **Obchod**   | Přepsání společnosti          | Přepsání společnosti                                                 |
| **Uživatel**    | Přepsání obchodu nebo společnosti | Nikdy                                                             |





