---
title: Plán pro globální adresář a další adresáře
description: Toto téma popisuje, co je třeba zvážit a jaká rozhodnutí je třeba učinit během procesu plánování.
author: msftbrking
ms.date: 01/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: sericks
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: brking
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1d3a476a183453f170dae9b812949822ea60edd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747602"
---
# <a name="plan-for-the-global-address-book-and-other-address-books"></a>Plán pro globální adresář a další adresáře

[!include [banner](../includes/banner.md)]

Toto téma popisuje, co je třeba zvážit a jaká rozhodnutí je třeba učinit během procesu plánování, před nastavením a konfigurací globálního adresáře a jakéhokoli dalšího adresáře. Některá rozhodnutí vyžadují potvrzení rozhodnutí, která byla učiněna pro další oblasti produktu, jako je například hierarchie organizace.

## <a name="global-address-book"></a>Globální adresář

Než začnete pracovat s globálním adresářem, je třeba určit pro něj výchozí hodnoty. Tyto výchozí hodnoty jsou následně použity pro všechny další adresáře, které vytvoříte.

**Rozhodnutí**

- V jakém pořadí se mají názvy zobrazit pro záznamy strany typu **Osoba**? Například jedna sekvence je příjmení, druhé jméno a křestní jméno.
- Mají být záznamy strany odstraněny z adresáře při odstranění záznamu role? Například pokud dojde k odstranění záznamu odběratele, má být záznam strany také odstraněn?
- Když je vytvořen nový záznam, má být uživatelům zasláno oznámení, je-li nalezen duplicitní záznam v globálním adresáři?
- Má být číslo systému univerzální číslování dat (DUNS) zahrnuto do informací pro záznam strany?
- Pokud je číslo DUNS zahrnuto v záznamu strany, je třeba ověřit jedinečnost čísla?
- Chcete při vytvoření záznamu strany v globálním adresáři použít výchozí typ strany, osoby nebo organizace?
- Které role uživatele by měly mít přístup k soukromým adresám a kontaktním informacím v záznamech strany?

## <a name="additional-address-books"></a>Další adresáře

Po vytvoření globálního adresáře můžete vytvořit další adresáře podle potřeby, například samostatný adresář pro každou společnost v organizaci a pro každé odvětví obchodu. Například společnost Fabrikam je mezinárodní organizace, která má více společností a více odvětví obchodu. Společnost Fabrikam plánuje vytvořit adresář pro každé odvětví obchodu. Pro odvětví obchodu realizované ve více než jednom místě, například odvětví pneumatických nástrojů, společnost Fabrikam plánuje vytvořit adresář pro každé místo. Chris, správce IT ve společnosti Fabrikam, vytvořil následující seznam adresářů, které jsou požadovány. Tento seznam také popisuje záznamy strany, které musí každý adresáře obsahovat.

- **Kontrakty veřejného sektoru (PubSC)** – Záznamy strany pro všechny strany, které jsou zahrnuty do kontraktů veřejného sektoru, které společnost Fabrikam získala.
- **Kontrakty soukromého sektoru (PriSC)** – Záznamy strany pro všechny strany, které jsou zahrnuty do kontraktů soukromého sektoru, které společnost Fabrikam získala.
- **Elektronické nástroje (ET)** – Strany záznamů pro všechny strany, která se účastní nákupu nebo prodeje elektronických nástrojů nebo jinak využívají elektronické nástroje, které poskytla nebo které nakupují pro společnost Fabrikam (Fabrikam – Japonsko).
- **Pneumatické nástroje (PTJPN)** – Strany záznamů pro všechny strany, která se účastní nákupu nebo prodeje pneumatických nástrojů nebo jinak využívají pneumatické nástroje, které poskytla nebo které nakupují pro společnost Fabrikam (Fabrikam – Japonsko).
- **Pneumatické nástroje (PTUSA)** – Strany záznamů pro všechny strany, která se účastní nákupu nebo prodeje pneumatických nástrojů nebo jinak využívají pneumatické nástroje, které poskytla nebo které nakupují pro společnost Fabrikam (Fabrikam – USA).

**Rozhodnutí:**

- Kolik dalších adresářů vytvoříte?


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]