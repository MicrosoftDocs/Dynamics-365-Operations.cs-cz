---
title: "Stránka se seznamem transakcí odběratele"
description: "Toto téma obsahuje informace o stránce se seznamem transakcí odběratele pro aplikaci Microsoft Dynamics 365 for Finance and Operations."
author: mikefalkner
manager: aolson
ms.date: 08/28/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: c6502a6fb0ceaed75fd5bb6ec5b2f13db1879eea
ms.openlocfilehash: 1b359939c867ba0a0c14859c83f0560afe6ba5be
ms.contentlocale: cs-cz
ms.lasthandoff: 10/12/2018

---

# <a name="customer-transactions-list-page"></a>Stránka se seznamem transakcí odběratele

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a>Zobrazit vyrovnání

Tlačítko **Zobrazit vyrovnání** v podokně akcí poskytuje rychlý přístup k historii vyrovnání a podrobné informace o celé transakci vyrovnání. Můžete také zobrazit další transakce, které souvisejí s vybranou transakcí, ať už proto, že byly součástí stejného vyrovnání, nebo protože jsou to platby, které byly vytvořeny ve stejném deníku plateb.

1. Zvolte **Pohledávky \> Všichni odběratelé**.
2. Vyberte odběratele, který má transakce, a poté v podokně akcí na kartě **Odběratel** zvolte **Transakce**.
3. Vyberte transakci pro průzkum a poté vyberte v podokně akcí **Zobrazit vyrovnání**.

    Zobrazí se dialogové okno **Zobrazit vyrovnání** a ukáže vybrané transakce a všechny doklady, proti kterým proběhlo vyrovnání. Toto dialogové okno připomíná zobrazení historie vyrovnání, ale obsahuje všechny související dokumenty.

4. V tomto dialogovém okně můžete provádět různé úkoly. Vyberte jeden nebo více dokladů a pak vyberte některou z následujících tlačítek:

    - **Zobrazit související** -Zobrazí se všechny transakce deníku plateb, které byly vytvořeny v deníku plateb souvisejícím se zvoleným dokumentem. Kromě toho se zobrazí všechna vyrovnání, která souvisejí s těmito platbami. Při zobrazení souvisejících plateb se změní popisek tohoto tlačítka na **Zobrazit vyrovnání**. Vyberte **Zobrazit vyrovnání**, chcete-li zobrazit pouze transakce, které byly zobrazeny při prvním otevření dialogového okna **Zobrazit vyrovnání**.
    - **Zobrazit historii** – Zobrazí historii vyrovnání pro doklady. Zvolte **Zavřít** a zavřete dialogové okno.
    - **Zobrazit účetnictví** – Zobrazí se všechny doklady, které souvisí se zvolenými dokumenty. Zvolte **Zavřít** a zavřete dialogové okno.
    - **Exportovat** – Exportujte vybrané doklady do aplikace Microsoft Excel.
    - **Vyrovnat transakce** – Toto tlačítko se zobrazí pouze v případě, že původní dokument, který byl vybrán, nebyl plně vyrovnán. Pokud zvolíte toto tlačítko, zobrazí se dialogové okno **Vyrovnat transakce**, kde lze vybrat transakce pro vyrovnání.
    - **Zrušit vyrovnání** – Toto tlačítko nabídka se zobrazí pouze v případě, že původní dokument, který byl vybrán, byl plně vyrovnán. Pokud zvolíte toto tlačítko, zobrazí se dialogové okno **Zrušit vyrovnání**, kde je možné zrušit vyrovnání, která byla vytvořena pro tento dokument.

## <a name="global-transactions"></a>Globální transakce

Tlačítko **Globální transakce** se také zobrazuje na stránce se seznamem **Transakce zákazníka**. Toto tlačítko vám umožňuje zobrazit všechny transakce odběratele napříč všemi právnickými osobami. Stránka se seznamem **Transakce odběratele** zobrazí transakce pouze pro právnické osoby, ke kterým má uživatel přístup, na základě jeho nastavení zabezpečení.

Stránka se seznamem zobrazí všechny transakce odběratele, které mají stejné ID strany jako odběratel, se kterým jste začali. Například pokud odběratel US-001 v jedné právnické osobě má stejné ID strany jako odběratel DE-001 v jiné právnické osobě, jsou zobrazeny všechny transakce pro obě ID odběratele.

Nabídky na stránce se seznamem **Transakce odběratele** se liší v závislosti na právnické osobě pro transakci. Například pokud je funkce k dispozici pouze pro švýcarské právnické osoby, možnosti nabídky pro tuto funkci se zobrazí pouze při výběru švýcarské transakce.

Chcete-li získat přístup k této funkci, postupujte takto.

1. Zvolte **Pohledávky \> Všichni odběratelé**.
2. Vyberte odběratele a poté v podokně akcí na kartě **Odběratel** ve skupině **Transakce** zvolte **Globální transakce**.

## <a name="more-transaction-filters"></a>Další filtry transakcí 

Filtr pro zobrazení otevřených transakcí byl nahrazen novým filtrem, který vám umožní zobrazit více kombinací transakcí. Následující možnosti jsou k dispozici v poli **Zobrazit**:

- **Všechny** – Zobrazí všechny transakce pro zvolené odběratele (otevřené a zavřené).
- **Uzavřené** – Zobrazuje pouze transakce, které byly plně vyrovnány a uzavřeny.
- **Otevřené** – Zobrazuje pouze transakce, které nebyly plně vyrovnány.
- **Otevřít včetně uzavřených nebo po datu** – zobrazí pouze transakce, které nebyly plně vypořádány k zadanému datu nebo po něm. Pokud vyberete tuto možnost, lze změnit datum, které je uvedeno vedle filtru. Transakce, které mají hodnotu **Poslední datum vyrovnání** po datu nebo k datu, které určíte, se zobrazí v seznamu i v případě, že tyto transakce jsou plně vyrovnány k aktuálnímu datu. Zůstatek však představuje zůstatky k aktuálnímu datu, nikoliv k vybranému datu.

Zaškrtněte políčko **Skrýt přecenění měny** ke skrytí transakcí převodu měny.

## <a name="modify-due-dates-and-discount-dates"></a>Změnit data splatnosti a data slevy

Data splatnosti a data slevy lze aktualizovat pro otevřené transakce odběratele. Ve verzi 8.1 nyní můžete přidat data splatnosti na stránku se seznamem **Transakce zákazníka**. Kliknutím na datum splatnosti na stránce se sezamem **Transakce odběratele** lze rovněž změnit data splatnosti, data slevy, platební podmínky a podmínky platební slevy v dialogovém okně **Aktualizovat datum splatnosti a data platební slevy**.

### <a name="activate-the-feature"></a>Aktivace funkce

Chcete-li přidat data splatnosti na stránce se seznamem **Transakce odběratele** změnit nastavení platby pro transakci pomocí dialogového okna **Aktualizovat datum splatnosti a data platební slevy**, postupujte podle těchto kroků.

1. Zvolte **Pohledávky \> Nastavení \> Parametry pohledávek**.
2. Na kartě **Vyrovnání** nastavte možnost **Zobrazit data splatnosti a povolit úpravy** na **Ano**.
3. Aby byla tato funkce povolena, byla přidána nová pole k transakcím odběratele. Tato pole se vyplní při dokončení nové transakce. Vyplní se rovněž tehdy, když otevřete dialogové okno **Aktualizovat datum splatnosti a data platební slevy**. Když nastavíte možnost **Zobrazit datum splatnosti a povolit úpravy** na **Ano**, zobrazí se dialogové okno **Aktualizovat informace o platbách**.  Pokud chcete aktualizovat existující transakce ihned, vyberte **Aktualizovat všechny existující transakce**. Pokud chcete vyplnit pole pouze pro nové transakce, vyberte **Pokračovat bez aktualizace**.

Datum splatnosti je nyní přidáno na stránku se seznamem **Transakce zákazníka**, takže můžete snadněji upravit datum splatnosti a datum platebních slev pro transakce.

### <a name="modify-the-payment-settings"></a>Úprav nastavení plateb

Stránka se seznamem **Transakce odběratele** zobrazí všechny transakce odběratele. Pokud vyberete datum splatnosti transakce, zobrazí se dialogové okno **Aktualizovat datum splatnosti a data platebních slev**. Toto dialogové okno zobrazí základní datum pro výpočet splatnosti výpočty a slevy, datum splatnosti, platební podmínky, podmínky platební slevy a data platební slevy.

Při úpravě má každé pole jiný účinek na transakci:

- **Upravit základní datum:** Datum splatnosti a data slevy se změní, jako kdyby základní datum bylo datem dokumentu.
- **Upravit datum splatnosti:** - Změní se pouze datum splatnosti.
- **Upravit data slevy:** Změní se pouze data slevy.
- **Upravit platební podmínky:** Změní se datum splatnosti na základě základního data a platebních podmínek.
- **Upravit podmínky platební slevy:** Platební slevy se změní na základě základního data a podmínek platební slevy.

Po dokončení úprav nastavení platby vyberte **Zavřít** pro uložení vašich změn.

