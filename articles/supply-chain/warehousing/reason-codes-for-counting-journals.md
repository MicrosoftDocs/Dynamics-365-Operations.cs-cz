---
title: Kódy důvodů pro inventury zásob
description: Toto téma popisuje, jak nastavit a použít kódy důvodů pro úlohy účtování.
author: perlynne
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCountingReasonCodePolicy, InventCountingReasonCode
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 4510ed7033e7c4e5187905906dcbef63f05a130bafcb7d9f19bbb360a7298119
ms.sourcegitcommit: fa5ff2a0822aac16b518a2aea0d3389f79793390
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/07/2021
ms.locfileid: "7012084"
---
# <a name="reason-codes-for-inventory-counting"></a>Kódy důvodů pro inventury zásob

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Kódy důvodů umožňují analyzovat výsledky procesu inventury a jakýkoli nesoulad, který se vyskytne během tohoto procesu. Můžete určit důvod pro provádění inventury, například rozbitou paletu nebo úpravu zásob, založenou na vzorku zásob. Současně můžete použít funkci úprav k zaúčtování hodnoty úprav množství na skladě na příslušný protiúčet na základě důvodu každé úpravy zásob.

## <a name="recommendation"></a>Doporučení

Před nastavením systému doporučujeme nejprve definovat strategii pro práci s kódy důvodu. Zkuste například zodpovědět následující otázky:

- Měly by být kódy důvodů povinné na skladech?
- Měly by být kódy důvodů povinné nebo volitelné na některých položkách?
- Kolik kódů důvodů vyžadujete?
- Musíte předem vybrat omezený seznam kódů důvodů pro úpravy?
- Jak by měli uživatelé čteček čárových kódů používat kódy důvodů? Měly by být kódy důvodů předvybrané, povinné nebo bez možnosti úpravy?
- Vyžadují pracovníci skladu různé chování kódů důvodů na mobilních čtečkách? Je-li odpověď ano, můžete vytvořit další položky nabídky a přiřadit je k různým osobám.
- Měly by kódy důvodu řídit zaúčtování finančních protiúčtů?

## <a name="turn-on-reason-code-features-in-your-system"></a>Zapnutí funkce kódu důvodu v systému

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Pokud ve svém systému nevidíte všechny funkce popsané v tomto tématu, pravděpodobně budete muset zapnout funkci *Zaúčtovat úpravy množství na skladě pomocí konfigurovatelných kódů důvodu připojených k protiúčtům*. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, je-li to potřeba. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Zaúčtovat úpravy množství na skladě pomocí konfigurovatelných kódů důvodu připojených k protiúčtům*

## <a name="set-up-reason-codes"></a>Nastavení kódů důvodů

### <a name="set-up-reason-code-policies"></a>Nastavení zásad kódů důvodů

Můžete vytvořit více zásad kódů důvodů, které budou řídit, kdy a jak se kódy důvodů inventury použijí. Každá zásada kódu příčiny může mít jeden ze dvou typů kódu důvodu inventury (*Volitelný* nebo *Povinný*). Zásady kódů důvodů inventury lze použít na úrovni skladu nebo na úrovni položky.

Chcete-li vytvořit zásadu kódu důvodu, postupujte takto.

1. Přejděte do nabídky **Řízení zásob** \> **Nastavení** \> **Zásoby** \> **Zásady kódů důvodů inventury**.
1. V podokně Akce vyberte možnost **Nový**. Tím se přidá zásada do mřížky.
1. Nastavte **Název** pro novou zásadu.
1. V poli **Typ kódu důvodů inventury** vyberte buď *Povinné* nebo *volitelné* a určete, zda výběr kódu důvodů má být volitelná nebo povinná akce v jednom z následujících procesů úpravy zásob:

    - Cyklická inventura (mobilní zařízení)
    - Místní inventura (mobilní zařízení)
    - Prahová inventura (mobilní zařízení)
    - Příchozí úprava (mobilní zařízení)
    - Odchozí úprava (mobilní zařízení)
    - Deník inventur (plně funkční klient)
    - Úprava množství/online sčítání (bohatý klient)

Zásady kódů důvodů můžete nastavit pro jednotlivé sklady i pro produkty. Nastavení kódu důvodu pro produkt může přepsat nastavení pro sklad produktu.

> [!NOTE]
> U skladů a položek, kde je nastaveno pole **Zásada kódu důvodů inventury** na *Povinné*, nelze deník inventur dokončit a uzavřít, dokud není zadán kód důvodu. Další informace naleznete v následující části.

### <a name="assign-counting-reason-code-policies-to-warehouses"></a>Přiřazení zásad kódu důvodu inventury ke skladům

Chcete li ke skladu přiřadit zásady kódu důvodu inventury, postupujte takto.

1. Přejděte do části **Řízení zásob** \> **Nastavení** \> **Rozdělení zásob** \> **Sklady**.
1. V podokně seznamu vyberte sklad.
1. V podokně Akce na kartě **Sklad** ve skupině **Nastavení** vyberte **Zásada kódu důvodů inventury**. Poté v rozevíracím dialogovém okně **Přiřadit zásadu kódu důvodu inventury** proveďte jeden z těchto kroků:

    - Chcete-li pomocí nastavení zásady u každé položky určit, zda jsou pro ni deníky inventury povinné, nezadávejte žádnou hodnotu (nebo odstraňte stávající hodnotu).
    - Chcete-li v denících inventury pro sklad vyžadovat kód důvodu, vyberte zásadu důvodu, kde je pole **Typ kódu důvodů inventury** nastaveno na *Povinný*.
    - Když je kód důvodu v denících inventury pro sklad nepovinný, vyberte zásadu důvodu, kde je pole **Typ kódu důvodů inventury** nastaveno na *Volitelný*.

### <a name="assign-counting-reason-code-policies-to-products"></a>Přiřazení zásad kódu důvodu inventury k produktům

Chcete li k produktu přiřadit zásady kódu důvodu inventury, postupujte takto.

1. Přejděte na **Řízení informací o produktech** \> **Produkty** \> **Uvolněné produkty**.
1. V mřížce vyberte produkt.
1. V podokně Akce na kartě **Produkt** ve skupině **Nastavení** vyberte **Zásada kódu důvodů inventury**. Poté v rozevíracím dialogovém okně **Přiřadit zásadu kódu důvodu inventury** proveďte jeden z těchto kroků:

    - Chcete-li pomocí nastavení zásady u každého skladu určit, zda jsou deníky inventury pro produkt povinné, nezadávejte žádnou hodnotu (nebo odstraňte stávající hodnotu).
    - Chcete-li v denících inventury pro produkt vyžadovat kód důvodu, vyberte zásadu důvodu, kde je pole **Typ kódu důvodů inventury** nastaveno na *Povinný*. Toto nastavení přepíše všechna nastavení kódu důvodu na úrovni skladu.
    - Když je kód důvodu v denících inventury pro produkt nepovinný, vyberte zásadu důvodu, kde je pole **Typ kódu důvodů inventury** nastaveno na *Volitelný*. Toto nastavení přepíše všechna nastavení kódu důvodu na úrovni skladu.

### <a name="set-up-counting-reason-codes"></a>Nastavení kódů důvodu inventury

Chcete-li nastavit kódy důvodu inventury, postupujte následujícím způsobem.

1. Přejděte do nabídky **Řízení zásob** \> **Nastavení** \> **Zásoby** \> **Kódy důvodů inventury**.
1. V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky.
1. Nastavte pole **Kód důvodu inventury** a **Popis** pro nový řádek.
1. Chcete-li přiřadit protiúčet, zadejte nebo vyberte hodnotu v poli **Protiúčet**.

    > [!NOTE]
    > Pokud je ke kódu důvodu inventury přiřazen protiúčet, je při zaúčtování do deníku inventury pod tímto kódem důvodu hodnota zaúčtována na přiřazený protiúčet namísto na výchozí profilový účet účtování inventáře.

### <a name="set-up-counting-reason-code-groups"></a><a name="reason-groups"></a>Nastavení skupin kódů důvodů inventury

*Skupiny kódů důvodu inventury* lze použít jako součást položek nabídky *Příchozí úprava* a *Odchozí úprava* v mobilní aplikaci Warehouse Management pro omezení seznamu kódů důvodů inventury. (Další informace o skupinách kódů důvodu inventury najdete v článku [Nastavení položek nabídky mobilního zařízení pro příchozí a odchozí úpravu](#setup-adjustment-in-out) dále v tomto tématu.)

1. Přejděte do nabídky **Řízení zásob** \> **Nastavení** \> **Zásoby** \> **Skupiny kódů důvodů inventury**.
1. V podokně Akce vyberte možnost **Nový** a přidejte skupinu.
1. Nastavte pole **Skupina důvodu inventury** a **Popis skupiny** pro novou skupinu.
1. V podokně akcí vyberte **Uložit**.
1. V části **Detaily** vyberte **Nový** na panelu nástrojů pro přidání řádku do mřížky. Poté nastavte pole **Kód důvodu inventury** pro nový řádek. 
1. Opakováním předchozího kroku přiřadíte podle potřeby více kódů. Pokud musíte odebrat kód ze skupiny, vyberte ho a pak vyberte příkaz **Odstranit** na panelu nástrojů.

### <a name="set-up-reason-codes-for-mobile-device-menu-items"></a>Nastavení kódů důvodu pro položky nabídky mobilního zařízení

Kódy důvodu můžete konfigurovat pro následující typy úprav množství na skladě:

- Cyklická inventura
- Místní inventura
- Prahová inventura
- Příchozí úprava
- Odchozí úprava

Ve většině případů můžete pro každou příslušnou položku nabídky mobilního zařízení definovat následující informace:

- Zda je kód důvodu zobrazen pro pracovníka na mobilním zařízení při inventuře.
- Výchozí kód důvodu, který se zobrazí na položce nabídky mobilního zařízení.
- Zda uživatel může upravit kód důvodu.

#### <a name="set-up-mobile-device-menu-items-for-a-counting-process"></a>Nastavení položek nabídky mobilního zařízení pro inventuru

Chcete-li nastavit položku nabídky mobilního zařízení pro inventuru, postupujte následujícím způsobem.

1. Přejděte do **Řízení skladu** \> **Nastavení** \> **Mobilní zařízení** \> **Položky nabídky mobilního zařízení**.
1. V podokně seznamu vyberte příslušnou položku nabídky nebo vytvořte novou položku.
1. V podokně Akce klikněte na možnost **Cyklická inventura**.
1. V poli **Výchozí kód důvodů inventury** nastavte výchozí kód důvodu, který má být zaznamenán při provádění inventury pomocí položky nabídky mobilního zařízení.
1. V poli **Zobrazit kód důvodů inventury** vyberte některou z následujících hodnot:

    - *Řádek* – Po zaznamenání každé odchylky ukázat kód důvodu.
    - *Skrýt* - Nezobrazit kód důvodu.

1. Nastavením možnosti **Upravit kód důvodů inventury** na *Ano* umožníte pracovníkovi upravovat kód důvodu, když se zobrazí během inventury na mobilním zařízení. Nastavte možnost na *Ne*, když pracovník nesmí kód upravit.

> [!NOTE]
> Tlačítko **Cyklická inventura** může být povoleno na jakékoliv položce nabídky mobilního zařízení, na kterém lze provést inventuru. Příklady zahrnují položky nabídky pro místní inventury, práci řízenou uživatelem a práci řízenou systémem.

#### <a name="set-up-mobile-device-menu-items-for-adjustment-in-and-adjustment-out"></a><a name="setup-adjustment-in-out"></a>Nastavení položek nabídky mobilního zařízení pro příchozí a odchozí úpravu

Chcete-li nastavit položku nabídky mobilního zařízení pro příchozí a odchozí úpravy, postupujte následujícím způsobem.

1. Přejděte do **Řízení skladu** \> **Nastavení** \> **Mobilní zařízení** \> **Položky nabídky mobilního zařízení**.
1. V podokně Akce vyberte možnost **Nová** a vytvořte novou položku nabídky.
1. Nastavte pole **Název mobilní položky** a **Nadpis** pro novou položku nabídky.
1. Nastavte pole **Režim** na *Práce*.
1. Nastavte hodnotu možnosti **Použít stávající práci** na *Ne*.
1. V poli **Proces pro vytvoření práce** vyberte *Příchozí úprava* nebo *Odchozí úprava*.
1. Na záložce **Obecné** zadejte následující pole. (Všechna tato pole se přidají, když vyberete hodnotu *Příchozí úprava* nebo *Odchozí úprava* v poli **Proces tvorby práce**.)

    - **Použít průvodce procesem** – Když vytváříte proces *Odchozí úprava*, nezapomeňte tuto možnost nastavit na *Ano*. Pokud vytváříte proces *Odchozí úprava*, je tato možnost vždy nastavena na *Ano*.
    - **Výchozí kód důvodů inventury** – Nastavte výchozí kód důvodu, který má být zaznamenán při provádění inventury pomocí položky nabídky mobilního zařízení.
    - **Zobrazit kód důvodů inventury** – Vyberte některou z následujících hodnot:

        - *Řádek* – Po zaznamenání každé odchylky ukázat kód důvodu.
        - *Skrýt* - Nezobrazit kód důvodu.

    - **Upravit kód důvodů inventury** – Nastavením této možnosti na *Ano* umožníte pracovníkovi upravovat kód důvodu, když se zobrazí během inventury na mobilním zařízení. Nastavte možnost na *Ne*, když pracovník nesmí kód upravit.
    - **Skupina kódů důvodu inventury** – Chcete -li omezit seznam možností, který se zobrazí pracovníkům, vyberte skupinu kódů důvodu. Informace o tom, jak nastavit skupiny kódů důvodu, najdete v části [Nastavení skupin kódů důvodů inventury](#reason-groups) dříve v tomto tématu. 

> [!NOTE]
> Když přiřadíte skupinu kódů důvodu inventury k položkám nabídky *Příchozí úprava* a *Odchozí úprava* a možnost **Použít průvodce procesem** je nastavena na *Ano*, získáte omezený seznam kódů důvodu inventury jako součást zpracování v mobilní aplikaci Warehouse Management.
>
> Možnost **Použít průvodce procesem** může také pomoci zabránit tomu, aby k velkému množství úprav došlo omylem. (Pracovník může například omylem naskenovat čárový kód čísla položky namísto hodnoty množství.) Chcete -li nastavit tuto funkci, nastavte možnost **Použít průvodce procesem** na *Ano* pro každou příslušnou položku nabídky. Pak přejděte na nabídku **Správa skladu \> Nastavení \> Pracovník** a nastavte pole **Limit množství úpravy** pro každého příslušného skladníka, a určete tak maximální množství úpravy, které může pracovník zaregistrovat.

## <a name="processing-that-uses-counting-reason-codes"></a>Zpracování, které používá kódů důvodu inventury

Když pracovníci používají mobilní aplikaci Warehouse Management, kódy důvodu se zaznamenávají. Pokud nebyl definován proces schvalování inventury, zaznamenané kódy důvodu jsou okamžitě použity jako součást účtování deníku inventury, které následuje.

### <a name="cycle-count-approvals"></a>Schválení cyklické inventury

Před schválením inventury může pracovník změnit kód důvodu, který je přidružen k inventuře. Po schválení inventury se zadává kód důvodu do řádků deníku inventur.

#### <a name="modify-reason-codes-for-cycle-count-approvals"></a>Úprava kódů důvodu pro schválení cyklické inventury

Chcete-li změnit schválení cyklické inventury, postupujte podle následujících pokynů.

1. Přejděte do nabídky **Řízení skladu** \> **Cyklická inventura** \> **Cyklická inventura práce čeká na kontrolu**.
1. V mřížce vyberte cyklickou inventuru.
1. V podokně akcí na kartě **Práce** zvolte **Cyklická inventura**. Poté v poli **Kód důvodu** vyberte nový kód důvodu.

Kódy důvodů jsou přidány do řádků deníku v denících inventur tyou *Deník inventur*.

1. Přejděte do nabídky **Řízení zásob** \> **Položky deníku** \> **Inventura zboží** \> **Inventura**.
2. V podrobnostech řádku deníku inventury vyberte v poli **Kód důvodu inventury** kód důvodu, který odpovídá vaší aktuální situaci.

### <a name="view-the-reason-codes-recorded-in-the-counting-history"></a>Zobrazení zaznamenaných kódů důvodu v historii inventury

Chcete-li zobrazit kódy důvodu, které byly zaznamenány v historii inventury, postupujte takto.

1. Přejděte na **Řízení zásob** \> **Dotazy a sestavy** \> **Historie inventury**.
1. Vyberte záznam počtu položek v podokně seznamu.
1. V poli **Kód důvodu inventury** uvidíte historii inventury, která byla zaznamenána prostřednictvím kódu důvodu.

### <a name="use-reason-codes-for-quantity-adjustment-or-online-counting"></a>Použití kódů důvodu k úpravě množství nebo online inventuře

Chcete-li použít kód důvodu pro úpravu množství nebo online inventuru, postupujte takto.

1. Přejděte na **Řízení zásob \> Dotazy a sestavy \> Zásoby na skladě**.
1. V podokně akcí zvolte **Úprava množství**.
1. Vyberte možnost **Úprava množství** a pak v poli **Kód důvodů inventury** vyberte kód důvodu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
