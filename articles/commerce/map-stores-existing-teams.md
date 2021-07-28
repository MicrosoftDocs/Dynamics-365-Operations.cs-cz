---
title: Mapování obchodů a týmů, pokud v Microsoft Teams již existují přednastavené týmy
description: Toto téma popisuje, jak mapovat obchody a odpovídající týmy v Dynamics 365 Commerce Headquarters, pokud vaše organizace již vytvořila týmy v Microsoft Teams před integrací s Commerce.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c75525749d9015387cc112beda104238a93698e9
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346685"
---
# <a name="map-stores-and-teams-if-there-are-pre-existing-teams-in-microsoft-teams"></a>Mapování obchodů a týmů, pokud v Microsoft Teams již existují přednastavené týmy

[!include [banner](includes/banner.md)]

Toto téma popisuje, jak mapovat obchody a odpovídající týmy v Dynamics 365 Commerce Headquarters, pokud vaše organizace již vytvořila týmy v Microsoft Teams před integrací s Commerce.

Před integrací Dynamics 365 Commerce a Microsoft Teams může vaše organizace mít vytvořené týmy pro některé nebo všechny vaše obchody. Pokud tomu tak je, musíte poskytnout mapování obchodů a odpovídající tým v Commerce Headquarters, pokud chcete vytvořit synchronizaci úkolů mezi Commerce POS a Microsoft Teams .

## <a name="map-stores-and-corresponding-teams-in-commerce-headquarters"></a>Mapování obchodů a odpovídajících týmů v Commerce Headquarters 

Pro mapování obchodů a odpovídajících týmů v Commerce Headquarters postupujte podle následujících kroků.

1. Přejděte do **Správa systému \> Pracovní prostor \> Správa dat**.
1. Vyberte **Export**. 
1. V podokně akcí zvolte **Nový**.
1. V možnosti **Název skupiny** zadejte „Exportovat mapování Teams“.
1. Na záložce s náhledem **Vybrané entity** vyberte **Přidat entitu**. Zobrazí se dialogové okno **Přidat entitu**.  
1. Z rozevíracího seznamu **Název entity** vyberte **Mapování Teams mezi zdrojem a týmem**.
1. V rozevíracím seznamu **Formát cílových dat** vyberte **CSV**.
1. Vyberte **Přidat** a potom vyberte **Zavřít**.
1. Vlevo nahoře pod podoknem akcí vyberte **Exportovat nyní**.
1. V možnosti **Stav zpracování entity** vyberte **Stáhnout soubor**.
1. V exportovaném souboru CSV zadejte hodnoty pro **SOURCETYPE**, **SOURCEID** a **TEAMID** následně:
    - Pro **SOURCETYPE** zadejte „RetailStore“. 
    - Pro **SOURCEID** zadejte číslo obchodu (například „000135“ pro obchod v San Francisku). Čísla obchodů najdete v možnostech **Retail a Commerce \> Kanály \> Obchody**.
    - Pro **TEAMID** zadejte odpovídající ID týmu z Microsoft Teams (například, "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c"). Informace o ID týmu najdete na [admin.teams.microsoft.com](https://admin.teams.microsoft.com).
1. Uložte soubor CSV do místního počítače.
1. Přejděte do **Správa systému \> Pracovní prostor \> Správa dat a poté zvolte** **Importovat**.
1. Na záložce s náhledem **Vybrané entity** vyberte **Přidat soubor**. Zobrazí se dialogové okno **Přidat soubor**.
1. Z rozevíracího seznamu **Název entity** vyberte **Mapování Teams mezi zdrojem a týmem**.
1. V rozevíracím seznamu **Formát zdrojových dat** vyberte **CSV**.
1. Vyberte **Nahrát a přidat**, vyberte soubor CSV, který jste dříve uložili, a poté vyberte **Otevřít**.
1. V dialogovém okně **Přidat soubor** vyberte **Zavřít**.
1. V podokně akcí vyberte **Uložit** a potom vyberte **Importovat**.

Následující příkladový obrázek ukazuje skupinu **Exportovat mapování Teams** v Commerce s prvky **Přidat entitu** a zvýrazněnými záhlavími exportovaného souboru CSV.

![Export mapování Teams v Commerce s prvky přidání entity a zvýrazněnými záhlavími exportovaného souboru CSV.](media/d365-commerce-data-mgmt-export-entity.png)

> [!NOTE]
> Po dokončení předchozích kroků postupujte podle pokynů v části [Synchronizace správy úkolů mezi Microsoft Teams a POS](synchronize-tasks-teams-pos.md) pro synchronizaci správy úkolů. 

## <a name="additional-resources"></a>Další prostředky

[Přehled integrace Dynamics 365 Commerce a Microsoft Teams](commerce-teams-integration.md)

[Povolení integrace Dynamics 365 Commerce a Microsoft Teams](enable-teams-integration.md)

[Zřízení Microsoft Teams z Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Synchronizace správy úkolů mezi Microsoft Teams a Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[Správa uživatelských rolí v Microsoft Teams](manage-user-roles-teams.md)

[Nejčastější dotazy k integraci Dynamics 365 Commerce a Microsoft Teams](teams-integration-faq.md)
