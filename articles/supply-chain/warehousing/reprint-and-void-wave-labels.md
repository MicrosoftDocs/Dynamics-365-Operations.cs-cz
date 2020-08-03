---
title: Opakovaný tisk a anulování vlnových štítků
description: Toto téma vysvětluje, jak zrušit a znovu vytisknout stávající vlnové štítky.
author: GarmMSFT
manager: PJacobse
ms.date: 07/09/2020
ms.topic: reprint-and-void-wave-labels
ms.service: dynamics-ax-applications
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate
audience: Application User
ms.reviewer: PJacobse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-olbara
ms.search.validFrom: 2020-07-09
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: 4c221a2817d71d79a5515379d2a33793660ebde5
ms.sourcegitcommit: 137e2bd30f0a85bd2e1baf1cf16b993edd2094f9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/09/2020
ms.locfileid: "3546412"
---
# <a name="reprint-and-void-wave-labels"></a>Opakovaný tisk a anulování vlnových štítků

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak spravovat štítky generované zpracováním vlny. (Podrobný popis a pokyny pro konfiguraci naleznete v části [Konfigurace tisku vlnových štítků](../warehousing/configure-wave-label-printing.md) .)

Vlnové štítky můžete kdykoli znovu vytisknout. Například pokud bude existující štítek ztracen nebo poškozen, pravděpodobně budete muset vytisknout jeden štítek. Alternativně by mohlo být nutné, aby pracovník nebo vedoucí skladu znovu vytiskl celou roli štítků, pokud by se počet a/nebo složení celé řady vlnových štítků změnily (například z důvodu nedostatku zásob nebo z jiných důvodů). Často, i když se změnil pouze počet kartonů, musí být celá role znovu vytištěna, aby byl celkový počet v části „Karton X Y“ každé etikety přesný.

Funkce opakovaného tisku vlnových štítků podporuje následující funkce:

- Opakovaně tiskněte štítky ze skladové aplikace i z bohatého klienta.
- Zrušte štítky a současně je znovu vytiskněte. (Schopnost zrušit štítky je například začleněná do scénářů krátkého výběru.)
- Vyčistěte historii vlnového štítku.

Toto téma představuje sbírku scénářů, které prostřednictvím příkladů ukazují, jak pracovat s funkcí opakovaného tisku vlnových štítků.

> [!IMPORTANT]
> Chcete-li zpracovat scénáře uvedené v tomto tématu, musíte nejprve zapnout a nakonfigurovat příslušné funkce tisku vlny, jak je popsáno v části [Konfigurace tisku vlnových štítků](../warehousing/configure-wave-label-printing.md). Několik scénářů v tomto tématu také vyžaduje, abyste nejprve prošli scénáře v tomto tématu a vytvořili předběžná vzorová data.

## <a name="scenario-1-reprint-labels-from-the-web-client"></a>Scénář 1: Opakovaný tisk štítků z webového klienta

vlnové štítky můžete zobrazit a znovu vytisknout z následujících stránek. V podokně akcí každé ze stránek **Dodávky** ve skupině **Související informace** vyberte **vlnové štítky**.

- Všechny zásilky \> Podrobnosti o zásilce
- Všechny náklady \> Načíst podrobnosti
- Všechny vlny
- Štítky vlny
- Historie popisků vlny

Chcete-li znovu vytisknout vlnový štítek z webového klienta, postupujte takto.

1. Přejděte na **Řízení skladu \> Výstupní vlny \> Vlny dodávek \> Všechny vlny**.
1. Vyberte vlnu, ze které chcete znovu vytisknout štítky.
1. V podokně akcí na kartě **Vlna** ve skupině **Tisk** zvolte **Vlnové štítky**.
1. Proveďte jeden nebo oba z následujících kroků:

    - Chcete-li štítek znovu vytisknout, vyberte tiskárnu v poli **Název tiskárny**. (Toto pole nechte prázdné, pokud chcete pouze aktualizovat podrobnosti o vlnovém štítku, aniž byste štítek znovu vytiskli.)
    - Chcete-li štítek aktualizovat, zaškrtněte políčko **Aktualizovat podrobnosti o vlnového štítku**. (Ponechte toto políčko nezaškrtnuté, pokud chcete znovu vytisknout předchozí štítek.)

    > [!NOTE]
    > Pokaždé, když se vlnový štítek vytiskne nebo znovu vytiskne, jeho data se převedou přes příslušné rozložení vlnového štítku a všechny zástupné symboly se nahradí skutečnými hodnotami. Výsledný řetězec je uložen jako záznam v historii vlnových štítků. Pokud políčko **Aktualizovat podrobnosti o vlnovém štítku** není zaškrtnuté, použijí se při opakovaném tisku štítku uložená data Zebra Programming Language (ZPL). Pokud je zaškrtnuto políčko **Aktualizovat podrobnosti o vlnovém štítku**, je vygenerován nový řetězec. Existující štítky vlnové štítky jsou také přepočítány a všechny nadbytečné štítky (například pokud byly související pracovní linie zrušeny nebo změněny) jsou označeny jako **Zrušené** a znovu se nevytisknou.

1. Výběrem **OK** svůj výběr potvrďte.

## <a name="scenario-2-reprint-labels-from-the-warehousing-app"></a>Scénář 2: Opakovaný tisk štítků ze skladové aplikace

Tento scénář se obvykle používá, pokud byla role štítků ztracena nebo poškozena. Poskytuje příklad, který ukazuje, jak nastavit položky nabídky mobilního zařízení, které zaměstnancům umožní opakovaný tisk jednoho a více štítků. Poté ukazuje, jak tyto nové položky nabídky používat, když pracujete na mobilním zařízení.

### <a name="set-up-the-required-menu-items-and-menu-for-the-mobile-device"></a>Nastavení požadovaných položky nabídky a nabídky pro mobilní zařízení

Než pracovníci mohou znovu vytisknout štítky z mobilního zařízení, musíte nastavit položky nabídky, abyste tuto funkci poskytli, a poté je přidat do nabídky skladové aplikace.

#### <a name="create-new-mobile-device-menu-items"></a>Vytvoření nových položek nabídky mobilních zařízení

Podle těchto kroků vytvořte novou kolekci položek nabídky pro opakovaný tisk štítků ze skladové aplikace.

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.
1. Vytvořte položku nabídky a nastavte pro ni následující hodnoty:

    - **Název položky nabídky:** *Opětovný tisk vlnového štítku*
    - **Titul:** *Opětovný tisk v jedné vlně*
    - **Režim:** *Nepřímý*
    - **Kód aktivity:** *Opětovný tisk v jedné vlně*

1. Vytvořte druhou položku nabídky a nastavte pro ni následující hodnoty:

    - **Název položky nabídky:** *Opakovaný tisk štítků (položka)*
    - **Titul:** *Opětovný tisk vlnových štítků (položka)*
    - **Režim:** *Nepřímý*
    - **Kód aktivity:** *Opětovný tisk ve více vlnách*
    - **Zobrazit filtr seskupení pracovního seznamu:** *Ano*
    - **Pole seskupení systému:** *ShipmentID*
    - **Popisek seskupení systému:** *ID dodávky*
    - **Režim tisku:** *Produkt*

1. V podokně akcí vyberte **Seznam polí** k otevření stránky, kde můžete vybrat pole, která se zobrazí, aby pracovníkům pomohla určit správnou roli štítků.
1. Můžete zobrazit až sedm polí. Pomocí rozevíracího seznamu vyberte pole, které se zobrazí na každé dostupné pozici. Nechte všechna pole, která nevyžadujete, prázdná. 

    Následuje příklad:

    - **Pole zobrazení:** *LabelItemId*
    - **Pole zobrazení 2:** *LabelItemName*
    - **Pole zobrazení 3:** *InventQty*
    - **Pole zobrazení 4:** *LabelUnitId*

1. Zavřete stránku.
1. Vytvořte třetí položku nabídky a nastavte pro ni následující hodnoty:

    - **Název položky nabídky:** *Opakovaný tisk štítků (výčet)*
    - **Titul:** *Opětovný tisk vlnových štítků (výčet)*
    - **Režim:** *Nepřímý**
    - **Kód aktivity:** *Opětovný tisk ve více vlnách*
    - **Zobrazit filtr seskupení pracovního seznamu:** *Ano*
    - **Pole seskupení systému:** *ShipmentID*
    - **Popisek seskupení systému:** *ID dodávky*
    - **Režim tisku:** *Výčet*

1. V podokně akcí vyberte **Seznam polí** a v rozevíracích seznamech vyberte pole, která se zobrazí na pomoc pracovníkům určit správnou roli štítků (například *LabelItemId*, *LabelItemName*, *InventQty*, *LabelUnitId* a *NumberOfLabels*).
1. Zavřete stránku.
1. Vytvořte čtvrtou položku nabídky a nastavte pro ni následující hodnoty:

    - **Název položky nabídky:** *Opakovaný tisk štítků (podle posledního)*
    - **Titul:** *Opětovný tisk vlnových štítků (podle posledního)*
    - **Režim:** *Nepřímý*
    - **Kód aktivity:** *Opětovný tisk ve více vlnách*
    - **Zobrazit filtr seskupení pracovního seznamu:** *Ano*
    - **Pole seskupení systému:** *ShipmentID*
    - **Popisek seskupení systému:** *ID dodávky*
    - **Režim tisku:** *ID poslední dobré vlny*

1. V podokně akcí vyberte **Seznam polí** a v rozevíracích seznamech vyberte pole, která se zobrazí na pomoc pracovníkům určit správnou roli štítků (například *LabelItemId*, *LabelItemName*, *InventQty*, *LabelUnitId* a *NumberOfLabels*).
1. Zavřete stránku.

#### <a name="set-up-the-mobile-device-menu"></a>Nastavení nabídky mobilního zařízení

Chcete-li přidat nové položky nabídky do nabídky skladové aplikace, postupujte následovně.

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Nabídka mobilního zařízení**.
1. Vyberte existující nabídku **Odchozí**.
1. V seznamu vlevo najděte položky nabídky opakovaného tisku, které jste právě vytvořili, a pomocí tlačítka se šipkou doprava je přidejte do seznamu na pravé straně.
1. Zavřete stránku.

### <a name="use-cases"></a>Případy použití

Zde uvedené případy použití uvádějí příklady, které ukazují, jak používat různé položky nabídky mobilního zařízení, které nastavíte, aby pracovníci mohli znovu tisknout vlnové štítky.

Než začnete tyto případy použití řešit, musí být splněny následující předpoklady:

- Musí být instalována ukázková data a musíte vybrat právnickou osobu **USMF**.
- Musí být nakonfigurován tisk vlnových štítků a některé štítky musí být generovány, jak je popsáno v části [Konfigurace tisku vlnových štítků](../warehousing/configure-wave-label-printing.md).

#### <a name="use-case-21-a-single-wave-label-is-scratched-and-must-be-reprinted"></a>Případ použití 2.1: Štítek jedné vlny poškrábaný a musí být znovu vytištěn.

1. Přihlaste se do skladové aplikace jako uživatel s přístupem ke skladu *62*. (Ve standardních ukázkových datech se můžete přihlásit pomocí ID uživatele *62* a hesla *1*.)
1. Přejděte na **Oudchozí \> Vytisknout jeden vlnový štítek**.
1. Zadejte nebo naskenujte ID vlnového štítku.
1. Vyberte tiskárnu, na které chcete tisknout.
1. Akci potvrďte výběrem tlačítka **OK**.

#### <a name="use-case-22-several-labels-for-boxes-of-the-same-item-were-damaged-and-must-be-reprinted-each-label-has-a-product-bar-code-but-no-enumeration-or-sscc-number"></a>Případ použití 2.2: Několik štítků pro krabice stejné položky bylo poškozeno a musí být znovu vytištěno. Každý štítek má čárový kód produktu, ale bez výčtu nebo čísla SSCC.

1. Přihlaste se do skladové aplikace jako uživatel s přístupem do skladu *62*. (Ve standardních ukázkových datech se můžete přihlásit pomocí ID uživatele *62* a hesla *1*.)
1. Přejděte na **Odchozí \> Znovu vytisknout štítky (položka)**.
1. Zadejte nebo naskenujte ID dodávky.
1. Vyberte dlaždici, která má správnou roli štítků, z níž budete znovu tisknout.
1. Naskenujte čárový kód produktu z existujícího štítku a ujistěte se, že byl vybrán správný řádek.
1. Zadejte počet štítků k opětovnému tisku.
1. Vyberte tiskárnu, na které chcete tisknout.
1. Akci potvrďte výběrem tlačítka **OK**.

#### <a name="use-case-23-several-labels-for-boxes-werent-printed-because-of-a-printer-jam-because-the-labels-have-enumeration-you-can-define-the-carton-range-to-reprint"></a>Příklad použití 2.3: Několik štítků pro krabice nebylo vytištěno kvůli zaseknutí tiskárny. Protože štítky mají výčet, můžete definovat rozsah kartonů pro opakovaný tisk.

1. Přihlaste se do skladové aplikace jako uživatel s přístupem do skladu *62*. (Ve standardních ukázkových datech se můžete přihlásit pomocí ID uživatele *62* a hesla *1*.)
1. Přejděte na **Odchozí \> Znovu vytisknout štítky (vyčíslení)**.
1. Zadejte nebo naskenujte ID dodávky.
1. Vyberte dlaždici, která má správnou roli štítků, z níž budete znovu tisknout.
1. Zadejte první krabici, pro kterou chcete štítek znovu vytisknout.
1. Zadejte poslední krabici, pro kterou chcete štítek znovu vytisknout. Toto pole můžete také ponechat prázdné, abyste znovu vytiskli štítky pro všechny kartony po určeném prvním kartonu.
1. Vyberte tiskárnu, na které chcete tisknout.
1. Akci potvrďte výběrem tlačítka **OK**.

#### <a name="use-case-24-several-labels-for-boxes-werent-printed-because-of-a-printer-jam-the-last-good-label-has-a-wave-label-id-that-is-printed-as-a-bar-code"></a>Příklad použití 2.4: Několik štítků pro krabice nebylo vytištěno kvůli zaseknutí tiskárny. Poslední dobrý štítek má ID vlnového štítku, který je vytištěn jako čárový kód.

1. Přihlaste se do skladové aplikace jako uživatel s přístupem do skladu *62*. (Ve standardních ukázkových datech se můžete přihlásit pomocí ID uživatele *62* a hesla *1*.)
1. Přejděte na **Odchozí \> Znovu vytisknout štítky (podle posledního)**.
1. Zadejte nebo naskenujte ID dodávky.
1. Vyberte dlaždici, která má správnou roli štítků, z níž budete znovu tisknout.
1. Zadejte nebo naskenujte ID posledního dobrého vlnového štítku. Aplikace identifikuje další štítek v sekvenci jako první karton, pro který bude štítek znovu vytištěn.
1. Zadejte poslední krabici, pro kterou chcete štítek znovu vytisknout. Toto pole můžete také ponechat prázdné, abyste znovu vytiskli štítky pro všechny kartony po určeném prvním kartonu.
1. Vyberte tiskárnu, na které chcete tisknout.
1. Akci potvrďte výběrem tlačítka **OK**.

## <a name="scenario-3-short-pick-and-reprint"></a>Scénář 3: Rychlý výběr a opakovaný tisk

Než začnete procházet tento scénář, musí být splněny následující předpoklady:

- Musí být instalována ukázková data a musíte vybrat právnickou osobu **USMF**.
- Musí být nakonfigurován tisk vlnových štítků a některé štítky musí být generovány, jak je popsáno v části [Konfigurace tisku vlnových štítků](../warehousing/configure-wave-label-printing.md).

### <a name="set-up-work-exceptions"></a>Nastavit pracovní výjimky

Výjimky z práce řídí chování rychlého výběru. Chcete-li nastavit pracovní výjimku, postupujte následujícím způsobem.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Práce \> Výjimky práce**.
1. Vytvořte záznam, který má následující nastavení:

    - **Kód pracovní výjimky:** *Rychlý výběr a tisk*
    - **Typ výjimky:** *Rychlý výběr*
    - **Navrhnout opětovný tisk vlnových štítků:** *Ano*

### <a name="void-and-reprint-after-a-short-pick"></a>Po rychlém výběru zrušit a vytisknout znovu

1. Přihlaste se do skladové aplikace jako uživatel s přístupem do skladu *62*. (Ve standardních ukázkových datech se můžete přihlásit pomocí ID uživatele *62* a hesla *1*.)
1. Otevřete pracovní postup zpracování pro vybraný pracovní příkaz, který byl vytvořen při původním tisku štítků.
1. Vyberte **Rychlý výběr**.
1. Vyberte kód pracovní výjimky, který jste vytvořili pro tento scénář.
1. Pokud jste vybrali správnou výjimku, mělo by být k dispozici zaškrtávací políčko **Zrušit a znovu vytisknout**. Zaškrtněte toto políčko a potvrďte. Po potvrzení je pořadí rolí štítků určené polem **ID sestavení štítku** přepočteno na základě změněných množství pracovní linky. Poté se znovu vytiskne na určené tiskárně.
