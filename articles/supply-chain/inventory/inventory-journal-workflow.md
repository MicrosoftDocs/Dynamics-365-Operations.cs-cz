---
title: Pracovní postupy schválení deníku zásob
description: Tento článek popisuje, jak nastavit s používat pracovní postupy schválení deníků pro různé typy transakcí fyzických zásob. Pracovní postupy deníku zásob zajišťují, že k transakcím mohou být zaúčtovány pouze schválené deníky zásob.
author: yufeihuang
ms.date: 07/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalTableWorkflowDropDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-07-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: ebb12562a9f06f2efc3b5a373d7ad0f98bc3505e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873978"
---
# <a name="inventory-journal-approval-workflows"></a>Pracovní postupy schválení deníku zásob

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak nastavit a používat pracovní postupy schválení deníku zásob pro různé typy transakcí fyzických zásob, jako například výdeje a příjmy, skladové pohyby, kusovníky a odsouhlasení fyzických zásob. Pracovní postupy deníku zásob zajišťují, že k transakcím mohou být zaúčtovány pouze schválené deníky zásob.

> [!NOTE]
> Pracovní postupy schvalování deníku zásob se vztahují pouze na transakce zaznamenané pomocí modulu Správa zásob. Nepracují s deníky zásob spuštěnými z modulu Řízení skladu.

## <a name="turn-on-the-inventory-journal-approval-workflows-feature"></a>Zapnutí funkce pracovních postupů schválení deníku zásob

Od verze Supply Chain Management 10.0.21 je tato funkce ve výchozím nastavení zapnuta. Správci mohou pomocí stránky [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a povolit či zakázat ji v případě potřeby. Tato funkce je uvedena jako:

- **Modul:** *Řízení zásob a skladu*
- **Název funkce:** *Pracovní postup schválení deníku zásob*

## <a name="create-your-inventory-journal-approval-workflows"></a>Vytvoření pracovních postupů schválení deníku inventáře

Chcete-li tuto funkci nastavit, musíte pro každý typ deníku zásob, který chcete ovládat, vytvořit pracovní postup. Protože různé typy deníku zásob mohou mít různé hierarchie schvalování a kroky pracovního postupu, můžete nakonfigurovat jednotlivé pracovní postupy pro každý typ deníku zásob.

Pracovní postupy podporují řízení verzí a každá z nich má ID pracovního postupu a aktivní verzi. Můžete si vybrat, zda chcete každou novou verzi pracovního postupu aktivovat okamžitě po vytvoření, nebo ji nechat neaktivní. Potřebujete-li pro stejný typ deníku různé pracovní postupy, vytvořte pro daný typ deníku více pracovních postupů a poté každý z nich přiřaďte jinému názvu deníku, který tento typ používá.

Vytvoření pracovních postupů schválení deníku inventáře:

1. Přejděte na **Řízení zásob \> Nastavení\> Pracovní postupy řízení zásob**.
1. V podokně akcí zvolte **Nový**.
1. Vyberte typ deníku zásob, pro který chcete nastavit pracovní postup:
    - **Deník inventur podle štítků**
    - **Deník změn vlastnictví zásob**
    - **Deník pohybu zásob**
    - **Deník převodu zásob**
    - **Deník inventury zásob**
    - **Deník kusovníků zásob**
    - **Deník úprav zásob**

    ![Dialogové okno Vytvořit pracovní postup.](media/journal-workflow-create-workflow.png "Dialogové okno Vytvořit pracovní postup")

1. Na vašem počítači se spustí aplikace editoru pracovního postupu. (Můžete být vyzváni, abyste tuto akci schválili.) Slouží k návrhu vašeho pracovního postupu podle potřeby. Podrobnosti o tom, jak používat editor pracovního postupu, viz [Přehled systému pracovního postupu](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).
1. Po uložení a zavření aplikace editoru pracovního postupu musíte zvolit, zda tuto verzi pracovního postupu aktivovat nebo ponechat jako neaktivní.

> [!NOTE]
> Pracovní postupy poskytují kontrolu verzí, což znamená, že si můžete zobrazit seznam verzí, které jste vytvořili, a vybrat, která z nich je aktivní. Chcete-li zobrazit seznam dostupných verzí a vybrat, které aktivovat, vyberte pracovní postup uvedený na stránce **Pracovní postupy řízení zásob**. V podokně akcí otevřete kartu **Pracovní postup** a vyberte **Verze**. Pro každou ID pracovního postupu může být současně aktivní pouze jedna verze.

## <a name="assign-approval-workflows-to-inventory-journal-names"></a>Pracovní postupy schválení názvů deníku zásob

Dalším krokem je přiřazení pracovního postupu deníku zásob ke každému názvu deníku zásob. Pro každý typ deníku zásob můžete nastavit více názvů deníku zásob.

Chcete-li přiřadit pracovní tok deníku zásob k názvu deníku zásob:

1. Přejděte na **Řízení zásob \> Nastavení \> Názvy deníků \> Zásoby**.
1. Chcete-li otevřít stránku nastavení, vyberte ze sloupce seznamu název deníku.
1. Na pevné záložce **Obecné** nastavte možnost **Pracovní postup schválení** na **Ano**. Vyberte **Ano** po zobrazení výzvy ke schválení akce.

    ![Přiřadit pracovní postup k názvu deníku.](media/journal-workflow-journal-name.png "Přiřadit pracovní postup k názvu deníku")

1. Otevřete rozevírací seznam **Pracovní postup** a vyberte požadovaný pracovní postup. Seznam zobrazuje každý aktivní pracovní postup, který jste vytvořili pomocí aplikace editoru pracovního postupu.

## <a name="create-an-inventory-journal-and-send-it-for-approval"></a>Vytvořte deník zásob a odešlete jej ke schválení

Jakmile přiřadíte název deníku zásob k odpovídajícímu pracovnímu postupu schvalování deníku zásob, budete moci vytvořit nové deníky zásob, které používají toto jméno, a poté tyto deníky odeslat pomocí tohoto pracovního postupu. Nebudete moci zaúčtovat deník zásob, dokud nebude schválen schvalovateli nakonfigurovanými v pracovním postupu.

1. V navigačním podokně rozbalte **Řízení zásob \> Zápisy v deníku \> Položky** a poté vyberte typ deníku zásob.
1. Vyberte **Nový** a vytvořte nový deník vybraného typu.
1. Otevře se dialogové okno **Vytvořit deník zásob**. Vyplňte formulář podle potřeby a poté vyberte **OK** k uložení deníku.
1. Podle potřeby vyplňte deník.
1. Když vytvoříte nebo otevřete deník zásob s přidruženým pracovním postupem schvalování, tlačítko **Pracovní postup** bude aktivní v podokně akcí. Až budete připraveni odeslat deník ke schválení, vyberte tlačítko **Pracovní postup** a otevřete rozevírací dialogové okno a poté vyberte **Odeslat**. Žádost o schválení pak směřuje k příslušnému schvalovateli, který bude upozorněn pomocí metody oznámení nakonfigurovaného pro pracovní postup.

    ![Předložení deníku ke schválení.](media/journal-workflow-inventory-journal.png "Předložení deníku ke schválení")

Chcete-li vyvolat žádost o schválení, otevřete příslušný deník, vyberte **Pracovní postup** a poté vyberte **Odvolání**. Tím se resetuje pracovní postup.

Až bude váš deník schválen, budete jej moci zveřejnit. Chcete-li zveřejnit deník, vyberte **Zveřejnit** z akčního podokna. Pokud není tlačítko **Zveřejnit** aktivní, deník nebyl dosud schválen.

## <a name="respond-to-an-inventory-journal-approval-request"></a>Odpověď na žádost o schválení deníku zásob

Pokud jste schvalovatelem, měli byste obdržet zprávu pokaždé, když je váš souhlas potřebný (jak je nakonfigurováno v příslušném pracovním postupu). Poté můžete schválit nebo zamítnout žádost o schválení deníku následujícím způsobem:

1. V navigačním podokně rozbalte **Řízení zásob \> Zápisy v deníku \> Položky** a poté vyberte typ deníku zásob.
1. Otevřete příslušný deník a přečtěte si jej.
1. Vyberte tlačítko **Pracovní postup** v podokně akcí a otevřete rozevírací dialogové okno. Vyberte jednu z následujících možností:
    - **Schválit** - shchválení žádosti.
    - **Odmítnout** - odmítnutí žádosti.
    - **Více \> Žádost o změnu** - Chcete-li odeslat žadateli zprávu s žádostí o změnu něčeho konkrétního a pak znovu odeslat.
    - **Více \> Delegovat** - Delegování schválení na jiného uživatele.
    - **Více \> Odvolat** - Odvolání žádosti o schválení (resetuje pracovní postup).
    - **Více \> Historie pracovního postupu** - Chcete-li zobrazit dosavadní historii tohoto pracovního postupu schvalování.

## <a name="review-the-approval-history"></a>Zkontrolujte historii schválení

Stejně jako u jiných typů pracovních postupů můžete použít stránku **Historie pracovního postupu** a zobrazit historii pracovního postupu schvalování pro jakýkoli deník.

Chcete-li zkontrolovat historii pracovního postupu pro deník:

1. V navigačním podokně rozbalte **Řízení zásob \> Zápisy v deníku \> Položky** a poté vyberte typ deníku zásob.
1. Otevření relevantní deník.
1. Vyberte tlačítko **Pracovní postup** v podokně akcí a otevřete rozevírací dialogové okno. Vyberte **Historii pracovního postupu**. Další informace viz [Historie pracovního postupu](../../fin-ops-core/fin-ops/organization-administration/tasks/view-workflow-history.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]