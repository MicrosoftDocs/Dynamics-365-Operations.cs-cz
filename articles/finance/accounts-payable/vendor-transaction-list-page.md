---
title: Stránka se seznamem transakcí dodavatele
description: Tento článek obsahuje informace o stránce se seznamem transakcí dodavatele pro Microsoft Dynamics 365 Finance.
author: sunfzam
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 34d9fd29f6a28bdd8c62e9460093544699dfeb2c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859936"
---
# <a name="vendor-transactions-list-page"></a>Stránka se seznamem transakcí dodavatele

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a>Zobrazit vyrovnání

Tlačítko **Zobrazit vyrovnání** v podokně akcí poskytuje rychlý přístup k historii vyrovnání a podrobné informace o celé transakci vyrovnání. Můžete také zobrazit další transakce, které souvisejí s vybranou transakcí, ať už proto, že byly součástí stejného vyrovnání, nebo protože jsou to platby, které byly vytvořeny ve stejném deníku plateb.

1. Zvolte **Závazky \> Všichni dodavatelé**.
2. Vyberte dodavatele, který má transakce, a poté v podokně akcí na kartě **Dodavatel** zvolte **Transakce**.
3. Vyberte transakci pro průzkum a poté vyberte v podokně akcí **Zobrazit vyrovnání**.

    Zobrazí se dialogové okno **Zobrazit vyrovnání** a ukáže vybrané transakce a všechny doklady, proti kterým proběhlo vyrovnání. Toto dialogové okno připomíná zobrazení historie vyrovnání, ale obsahuje všechny související dokumenty.

4. V tomto dialogovém okně můžete provádět různé úkoly. Vyberte jeden nebo více dokladů a pak vyberte některou z následujících tlačítek:

    - **Zobrazit související** – Zobrazí všechny transakce deníku plateb a transakce hlavní knihy pro dodavatele, které byly vytvořeny v denících, ve kterých byly vytvořeny dokumenty zobrazené v seznamu. Když je například zobrazena platba, pak se zobrazí všechny platby v deníku plateb, ve kterém byly vytvořeny. Pokud je zobrazena faktura nebo platba a byly vytvořeny v hlavním deníku, zobrazí se všechny dokumenty v hlavní knize, ve které byly vytvořeny. Také se zobrazí všechna vyrovnání, která souvisejí se seznamem dokumentů. Při zobrazení souvisejících plateb se změní popisek tohoto tlačítka na **Zobrazit vyrovnání**. Vyberte **Zobrazit vyrovnání**, chcete-li zobrazit pouze transakce, které byly zobrazeny při prvním otevření dialogového okna **Zobrazit vyrovnání**.
    - **Zobrazit historii** – Zobrazí historii vyrovnání pro doklady. Zvolte **Zavřít** a zavřete dialogové okno.
    - **Zobrazit účetnictví** – Zobrazí se všechny doklady, které souvisí se zvolenými dokumenty. Zvolte **Zavřít** a zavřete dialogové okno.
    - **Exportovat** – Exportujte vybrané doklady do aplikace Microsoft Excel.
    - **Vyrovnat transakce** – Toto tlačítko se zobrazí pouze v případě, že původní dokument, který byl vybrán, nebyl plně vyrovnán. Pokud zvolíte toto tlačítko, zobrazí se dialogové okno **Vyrovnat transakce**, kde lze vybrat transakce pro vyrovnání.
    - **Zrušit vyrovnání** – Toto tlačítko nabídka se zobrazí pouze v případě, že původní dokument, který byl vybrán, byl plně vyrovnán. Pokud zvolíte toto tlačítko, zobrazí se dialogové okno **Zrušit vyrovnání**, kde je možné zrušit vyrovnání, která byla vytvořena pro tento dokument.

## <a name="global-transactions"></a>Globální transakce

Tlačítko **Globální transakce** se také zobrazuje na stránce se seznamem **Transakce dodavatele**. Toto tlačítko vám umožňuje zobrazit všechny transakce dodavatele napříč všemi právnickými osobami. Stránka se seznamem **Transakce dodavatele** zobrazí transakce pouze pro právnické osoby, ke kterým má uživatel přístup, na základě jeho nastavení zabezpečení.

Stránka se seznamem zobrazí všechny transakce dodavatele, které mají stejné ID strany jako dodavatel, se kterým jste začali. Například pokud dodavatel US-001 v jedné právnické osobě má stejné ID strany jako dodavatel DE-001 v jiné právnické osobě, jsou zobrazeny všechny transakce pro obě ID dodavatele.

Nabídky na stránce se seznamem **Transakce dodavatele** se liší v závislosti na právnické osobě pro transakci. Například pokud je funkce k dispozici pouze pro švýcarské právnické osoby, možnosti nabídky pro tuto funkci se zobrazí pouze při výběru švýcarské transakce.

Chcete-li získat přístup k této funkci, postupujte takto.

1. Zvolte **Závazky** \> **Všichni dodavatelé**.
2. Vyberte dodavatele a poté v podokně akcí na kartě **Dodavatel** ve skupině **Transakce** zvolte **Globální transakce**.

## <a name="more-transaction-filters"></a>Další filtry transakcí

Filtr pro zobrazení otevřených transakcí byl nahrazen novým filtrem, který vám umožní zobrazit více kombinací transakcí. Následující možnosti jsou k dispozici v poli **Zobrazit**:

- **Všechny** – Zobrazí všechny transakce pro zvolené dodavatele (otevřené a zavřené).
- **Uzavřené** – Zobrazuje pouze transakce, které byly plně vyrovnány a uzavřeny.
- **Otevřené** – Zobrazuje pouze transakce, které nebyly plně vyrovnány.
- **Otevřít včetně uzavřených nebo po datu** – zobrazí pouze transakce, které nebyly plně vypořádány k zadanému datu nebo po něm. Pokud vyberete tuto možnost, lze změnit datum, které je uvedeno vedle filtru. Transakce, které mají hodnotu **Poslední datum vyrovnání** po datu nebo k datu, které určíte, se zobrazí v seznamu i v případě, že tyto transakce jsou plně vyrovnány k aktuálnímu datu. Zůstatek však představuje zůstatky k aktuálnímu datu, nikoliv k vybranému datu.

Zaškrtněte políčko **Skrýt přecenění měny** ke skrytí transakcí převodu měny.

## <a name="modify-due-dates-and-discount-dates"></a>Změnit data splatnosti a data slevy

Data splatnosti a data slevy lze aktualizovat pro otevřené transakce odběratele. Ve verzi 8.1 nyní můžete přidat data splatnosti na stránku se seznamem **Transakce dodavatele**. Kliknutím na datum splatnosti na stránce se sezamem **Transakce dodavatele** lze rovněž změnit data splatnosti, data slevy, platební podmínky a podmínky platební slevy v dialogovém okně **Aktualizovat datum splatnosti a data platební slevy**.

### <a name="activate-the-feature"></a>Aktivace funkce

Chcete-li přidat data splatnosti na stránce se seznamem **Transakce dodavatele** změnit nastavení platby pro transakci pomocí dialogového okna **Aktualizovat datum splatnosti a data platební slevy**, postupujte podle těchto kroků.

1. Zvolte **Závazky \> Nastavení \> Parametry závazků**.
2. Na kartě **Vyrovnání** nastavte možnost **Zobrazit data splatnosti a povolit úpravy** na **Ano**.
3. Aby byla tato funkce povolena, byla přidána nová pole k transakcím dodavatele. Tato pole se vyplní při dokončení nové transakce. Vyplní se rovněž tehdy, když otevřete dialogové okno **Aktualizovat datum splatnosti a data platební slevy**. Když nastavíte možnost **Zobrazit datum splatnosti a povolit úpravy** na **Ano**, zobrazí se dialogové okno **Aktualizovat informace o platbách**.  Pokud chcete aktualizovat existující transakce ihned, vyberte **Aktualizovat všechny existující transakce**. Pokud chcete vyplnit pole pouze pro nové transakce, vyberte **Pokračovat bez aktualizace**.

Datum splatnosti je nyní přidáno na stránku se seznamem **Transakce dodavatele**, takže můžete snadněji upravit datum splatnosti a datum platebních slev pro transakce.

### <a name="modify-the-payment-settings"></a>Úprav nastavení plateb

Stránka se seznamem **Transakce dodavatele** zobrazí všechny transakce dodavatele. Pokud vyberete datum splatnosti transakci, zobrazí se dialogové okno. Toto dialogové okno zobrazí základní datum pro výpočet splatnosti výpočty a slevy, datum splatnosti, platební podmínky, podmínky platební slevy a data platební slevy.

Při úpravě má každé pole jiný účinek na transakci:

- **Upravit základní datum:** Datum splatnosti a data slevy se změní, jako kdyby základní datum bylo datem dokumentu.
- **Upravit datum splatnosti:** - Změní se pouze datum splatnosti
- **Upravit data slevy:** Změní se pouze data slevy.
- **Upravit platební podmínky:** Změní se datum splatnosti na základě základního data a platebních podmínek.
- **Upravit podmínky platební slevy:** Platební slevy se změní na základě základního data a podmínek platební slevy.

Po dokončení úprav nastavení platby vyberte **Zavřít** pro uložení vašich změn.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
