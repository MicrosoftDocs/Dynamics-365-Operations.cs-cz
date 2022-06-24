---
title: Nastavení pokladního místa (POS) a uživatelského jazyka
description: Tento článek popisuje, jak změnit nastavení jazyka v Modern POS (MPOS) a Cloud POS.
author: jblucher
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 15490885b5ce366edbab669893f3c3e36585f308
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863340"
---
# <a name="point-of-sale-pos-application-and-user-language-settings"></a>Nastavení pokladního místa (POS) a uživatelského jazyka

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak změnit nastavení jazyka v Modern POS (MPOS) a Cloud POS.

## <a name="overview"></a>Přehled
Modern POS (MPOS) a Cloud POS podporují prostředí, kde se může nastavení jazyka a překlady lišit mezi nastavením obchodu a uživatelským nastavením. Obchod se může například nacházet v oblasti, kde zákazníci preferují angličtinu, ale někteří pracovníci dávají přednost používání aplikací s francouzskými překlady.

## <a name="data-language"></a>Jazyk dat

Bez ohledu na uživatelské nastavení bude MPOS a Cloud POS vždy používat nastavení jazyka obchodu k určení překladů používaných pro data. Tím se zajistí, že všichni uživatelé a zákazníci budou mít konzistentní zkušenosti. Příklady popisů dat:

- Produkty
- Atributy a hodnoty
- Názvy kategorie
- Tištěné nebo e-mailem odeslané transakční příjmy
- Názvy způsobu platby
- Zprávy řádkového displeje

Jazyk obchodu bude použit také pro hlavní přihlašovací obrazovku POS, protože uživatel není znám před přihlášením. Pokud překlad není k dispozici pro jazyk obchodu, POS se vrátí k jazyku společnosti.

### <a name="configuring-the-stores-language-setting"></a>Konfigurace nastavení jazyka obchodu

Jazyko obchodu se nastavuje ve složce **Všechny obchody** na stránce **Obchod** v části **Obecné &gt; Regionální nastavení &gt; Jazyk**. Pomocí rozevíracího seznamu vyberte jazyk pro každý obchod.

## <a name="user-interface-language"></a>Jazyk uživatelského rozhraní

Nastavení jazyka uživatele POS určuje překlady používané v uživatelském rozhraní aplikace. Jedná se o všechny popisky, nabídky a seznamy, které nejsou považovány za data. Jedinou výjimkou je text, který je zobrazen na tlačítkách mřížky POS. Tlačítka mřížky nepodporují překlady, takže budou vždy zobrazovaly text definovaný na tlačítku. Abyste získali podporu přeložených tlačítek, budete muset zkopírovat a udržovat samostatné mřížky tlačítek a přiřadit je uživatelům podle potřeby.

### <a name="configuring-the-users-language-setting"></a>Konfigurace nastavení jazyka uživatele

Nastavení jazyka uživatele POS pochází z nabídky **Všichni pracovníci** na stránce **Pracovník** v části **Maloobchod a velkoobchod &gt; Jazyk**. Není nastaveno na hlavní kartě Profil. Toto nastavení není použito v programu POS. Pokud není jazyk uživatele nastaven, nebo pokud je nastaven na jazyk, pro který nejsou k dispozici překlady, POS obnoví používání jazyka obchodu.

| &nbsp;      | Jazyk UR                  | Jazyk dat (produkty, formáty příjemky, řádkový displej atd.) |
|-------------|----------------------------|---------------------------------------------------------------|
| **Company (Společnost)** | Výchozí                    | Výchozí                                                       |
| **Obchod**   | Přepsání společnosti          | Přepsání společnosti                                             |
| **Uživatel**    | Přepsání obchodu nebo společnosti | Nikdy                                                         |


[!INCLUDE[footer-include](../includes/footer-banner.md)]