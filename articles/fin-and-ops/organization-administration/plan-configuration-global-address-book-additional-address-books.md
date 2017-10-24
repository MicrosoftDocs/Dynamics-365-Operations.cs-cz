---
title: "Plán konfigurace globálního adresáře a dalších adresářů"
description: "Tento článek popisuje, co je třeba zvážit a jaká rozhodnutí je třeba učinit během procesu plánování, před nastavením a konfigurací globálního adresáře a jakéhokoli dalšího adresáře v aplikaci Microsoft Dynamics 365 for Finance and Operations. Některá rozhodnutí vyžadují potvrzení rozhodnutí, která byla učiněna pro další oblasti produktu, jako je například hierarchie organizace."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: shiva.pandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 12bd0a02899c04b0511e2a50bc4a724d5074d13e
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="plan-how-to-configure-the-global-address-book-and-additional-address-books"></a>Plán konfigurace globálního adresáře a dalších adresářů

[!include[banner](../includes/banner.md)]


Tento článek popisuje, co je třeba zvážit a jaká rozhodnutí je třeba učinit během procesu plánování, před nastavením a konfigurací globálního adresáře a jakéhokoli dalšího adresáře v aplikaci Microsoft Dynamics 365 for Finance and Operations. Některá rozhodnutí vyžadují potvrzení rozhodnutí, která byla učiněna pro další oblasti produktu, jako je například hierarchie organizace.

<a name="global-address-book"></a>Globální adresář
-------------------

Než začnete pracovat s globálním adresářem, je třeba určit pro něj výchozí hodnoty. Tyto výchozí hodnoty jsou následně použity pro všechny další adresáře, které vytvoříte. 

**Rozhodnutí:**

-   V jakém pořadí se mají názvy zobrazit pro záznamy strany typu **Osoba**? Například jedna sekvence je příjmení, druhé jméno a křestní jméno.
-   Mají být záznamy strany odstraněny z adresáře při odstranění záznamu role? Například pokud dojde k odstranění záznamu odběratele, má být záznam strany také odstraněn?
-   Když je vytvořen nový záznam, má být uživatelům zasláno oznámení, je-li nalezen duplicitní záznam v globálním adresáři?
-   Má být číslo systému univerzální číslování dat (DUNS) zahrnuto do informací pro záznam strany?
-   Pokud je číslo DUNS zahrnuto v záznamu strany, je třeba ověřit jedinečnost čísla?
-   Chcete při vytvoření záznamu strany v globálním adresáři použít výchozí typ strany, osoby nebo organizace?
-   Které role uživatele by měly mít přístup k soukromým adresám a kontaktním informacím v záznamech strany?

## <a name="additional-address-books"></a>Další adresáře
Po vytvoření globálního adresáře můžete vytvořit další adresáře podle potřeby, například samostatný adresář pro každou společnost v organizaci a pro každé odvětví obchodu. Například společnost Fabrikam je mezinárodní organizace, která má více společností a více odvětví obchodu. Společnost Fabrikam plánuje vytvořit adresář pro každé odvětví obchodu. Pro odvětví obchodu realizované ve více než jednom místě, například odvětví pneumatických nástrojů, společnost Fabrikam plánuje vytvořit adresář pro každé místo. Chris, správce IT ve společnosti Fabrikam, vytvořil následující seznam adresářů, které jsou požadovány. Tento seznam také popisuje záznamy strany, které musí každý adresáře obsahovat.

-   **Kontrakty veřejného sektoru (PubSC)** – Záznamy strany pro všechny strany, které jsou zahrnuty do kontraktů veřejného sektoru, které společnost Fabrikam získala.
-   **Kontrakty soukromého sektoru (PriSC)** – Záznamy strany pro všechny strany, které jsou zahrnuty do kontraktů soukromého sektoru, které společnost Fabrikam získala.
-   **Elektronické nástroje (ET)** – Strany záznamů pro všechny strany, která se účastní nákupu nebo prodeje elektronických nástrojů nebo jinak využívají elektronické nástroje, které poskytla nebo které nakupují pro společnost Fabrikam (Fabrikam – Japonsko).
-   **Pneumatické nástroje (PTJPN)** – Strany záznamů pro všechny strany, která se účastní nákupu nebo prodeje pneumatických nástrojů nebo jinak využívají pneumatické nástroje, které poskytla nebo které nakupují pro společnost Fabrikam (Fabrikam – Japonsko).
-   **Pneumatické nástroje (PTUSA)** – Strany záznamů pro všechny strany, která se účastní nákupu nebo prodeje pneumatických nástrojů nebo jinak využívají pneumatické nástroje, které poskytla nebo které nakupují pro společnost Fabrikam (Fabrikam – USA).

**Rozhodnutí:**

-   Kolik dalších adresářů vytvoříte?

### <a name="address-book-security"></a>Zabezpečení adresáře

Adresáře můžete vytvořit kdykoli a také můžete kdykoli nastavit parametry zabezpečení adresáře. Nemusíte nastavit oprávnění zabezpečení pro adresář. Pokud tak neučiníte, všichni pracovníci ve vaší organizaci budou moci zobrazit všechny záznamy strany v tomto adresáři. Můžete nastavit oprávnění zabezpečení v záznamech strany prostřednictvím adresáře. Oprávnění zabezpečení jsou založena na týmech. Tento přístup zaručuje, že pouze zaměstnanci, kteří jsou přiřazeni do týmu, který má přístup k adresáři, budou moci zobrazit záznamy strany v tomto adresáři. Je třeba vybrat týmy, které mají přístup k jednotlivým adresářům. Pro každý adresář můžete nastavit oprávnění zabezpečení, která povolují nebo zakazují přístup k určitým týmům. Pokud udělíte týmu oprávnění k adresáři, všichni členové tohoto týmu budou moci zobrazit záznamy v daném adresáři. Pokud neudělíte týmu přístup k adresáři, členové tohoto týmu nebudou moci zobrazit záznamy v daném adresáři ani jeho obsah. 

**Rozhodnutí:**

-   Které týmy by měly mít přístup ke každému novému adresáři, který vytvoříte?





