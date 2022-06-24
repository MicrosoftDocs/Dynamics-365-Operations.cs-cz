---
title: Automatické přidělování poplatků
description: Funkce poplatků v Microsoft Dynamics 365 Supply Chain Management pomáhá vám automaticky přidělit poplatky nákupním objednávkám nebo prodejním objednávkám.
author: GalynaFedorova
ms.date: 09/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2020-10-01
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a0dd10ba7ce0f6eca2549edb227eb9116edea2d7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857481"
---
# <a name="automatic-allocation-of-charges"></a>Automatické přidělování poplatků

[!include [banner](../includes/banner.md)]

Na základě zákazníka, se kterým pracujete, nebo položky, kterou prodáváte, možná budete chtít uplatnit konkrétní dodatečné poplatky. Funkce *poplatků* v Microsoft Dynamics 365 Supply Chain Management pomáhá vám automaticky přidělit poplatky nákupním objednávkám nebo prodejním objednávkám.

Automatické náklady, které se nazývají automatické náklady, se používají automaticky při vytváření prodejní nebo nákupní objednávky. Automatické poplatky lze definovat pro konkrétní dodavatele, odběratele, skupiny dodavatelů nebo položek. Můžete také definovat automatické poplatky, které platí pro všechny dodavatele, odběratele nebo položky.

## <a name="set-up-parameters"></a>Nastavit parametry

Stránka **Parametry modulu Zásobování a zdroje** obsahuje několik nastavení, která jsou zvláště důležitá, když chcete přidělit poplatky automaticky. Abyste dokončili toto nastavení, postupujte takto.

1. Přejděte na **Zásobování a zdroje \> Nastavení \> Parametry modulu Zásobování a zdroje**.
1. Otevřete kartu **Ceny**.
1. Na záložce **Ceny** proveďte následující nastavení:
    - **Vyhledat automatické náklady pro záhlaví** - Určuje, zda poplatky pro záhlaví nákupních objednávek mají být automaticky přidělovány. Nastavte na *Ano*, chcete-li používat automatické přidělování poplatků.
    - **Vyhledat automatické náklady pro řádek** - Určuje, zda poplatky pro řádky nákupních objednávek mají být automaticky přidělovány. Nastavte na *Ano*, chcete-li používat automatické přidělování poplatků.

## <a name="set-up-charges-codes"></a>Nastavení kódů poplatků

Chcete-li přidělit poplatky, musíte nejprve definovat kódy poplatků.

1. Proveďte jeden z následujících kroků:

    - Nákupní objednávky: Přejděte na **Závazky \> Nastavení poplatků \> Kód poplatků**.
    - Prodejní objednávky: Přejděte na **Pohledávky \> Nastavení poplatků \> Kód poplatků**.

1. V podokně Akce vyberte možnost **Nová**, vytvoří se nový kód poplatků.
1. V záhlaví nového záznamu nastavte následující pole:

    - **Kód poplatků** - Zadejte kód poplatků.
    - **Popis** - zadejte popis poplatků.
    - **Skupina DPH položky** - Pokud je to možné, vyberte skupinu DPH položky.
    - **Poměrné** - Nastavte tuto možnost na *Ano*, pokud chcete poměrně rozdělit své poplatky. Tato možnost je k dispozici pouze pro prodejní objednávky.
    - **Maximální částka** - Zadejte maximální částku povolenou pro kód poplatku. Toto pole se používá k ověření poplatků za faktury dodavatele. Je k dispozici pouze pro nákupní objednávky.

        > [!NOTE]
        > Chcete-li zapnout funkci pro ověřování poplatků za nákupní objednávky, přejděte na **Závazky \> Nastavení \> Parametry závazků**. Na pevné záloce **Ověření faktury** v sekci **Ověření faktury** nastavte možnost **Povolit ověřování shody faktur** na *Ano*.

1. Pevná záložka **Zaúčtování** obsahuje sekce **Debet** a **Kredit**. Nastavte následující pole v závislosti na účetní knize, do které chcete účtovat poplatky:

    - **Typ** - Vyberte typ účtu, na který účtujete (*Účetní kniha*, *Zákazník* nebo *Položka*).
    - **Zaúčtování** - Vyberte typ účetního zápisu, který chcete vytvořit (např *Zprostředkovatelský poplatek* nebo *Vypořádání zákazníka*).
    - **Účet** - Vyberte účet, pro který chcete zaúčtovat poplatek.

1. V podokně akcí vyberte **Uložit**.

## <a name="create-charge-groups"></a>Vytvořte skupiny poplatků

Skupiny poplatků automaticky přidělují konkrétní poplatky skupině zákazníků nebo prodejců. Následující podsekce popisují, jak vytvořit a přiřadit tyto skupiny poplatků.

### <a name="charge-groups-for-purchase-orders"></a>Skupiny poplatků pro nákupní objednávky

Chcete-li vytvořit skupiny poplatků pro nákupní objednávky, postupujte takto.

1. Přejděte na **Závazky \> Nastavení poplatků \> Skupina poplatků dodavatele**.
1. V podokně Akce vyberte možnost **Nový** pro přidání řádku do mřížky a pak nastavte následující pole:

    - **Skupina poplatků** - Zadejte název skupiny poplatků.
    - **Popis** - zadejte popis skupiny poplatků.

1. V podokně akcí vyberte **Uložit**.
1. Přejděte na **Závazky \> Prodejci \> Všichni prodejci** a buď otevřete existujícího dodavatele, nebo vytvořte nového dodavatele.
1. Na pevné záložce **Výchozí nastavení nákupní objednávky** v sekci **Nákupní objednávka** nastavte pole **Skupina poplatků** na skupinu poplatků, kterou jste právě vytvořili.

### <a name="charge-groups-for-sales-orders"></a>Skupiny poplatků pro prodejní objednávky

Chcete-li vytvořit skupiny poplatků pro prodejní objednávky, postupujte takto.

1. Přejděte na **Pohledávky \> Nastavení poplatků \> Skupiny poplatků zákazníků**.
1. V podokně Akce vyberte možnost **Nový** pro přidání řádku do mřížky a pak nastavte následující pole:

    - **Skupina poplatků** - Zadejte název skupiny poplatků.
    - **Popis** - zadejte popis skupiny poplatků.

1. V podokně akcí vyberte **Uložit**.
1. Přejděte na **Pohledávky \> Zákazníci \> Všichni zákazníci** a buď otevřte stávajícího zákazníka, nebo vytvořte nového zákazníka.
1. Na pevné záložce **Výchozí nastavení nákupní objednávky** v sekci **Peodejní objednávka** nastavte pole **Skupina poplatků** na skupinu poplatků, kterou jste právě vytvořili.

## <a name="define-auto-charges"></a>Definování automatických poplatků

Po nastavení kódů poplatků definujte automatické poplatky podle těchto kroků.

1. Proveďte jeden z následujících kroků:

    - Nákupní objednávky: Přejděte na **Zásobování a zdroje \> Nastavení \> Poplatky \> Automatické poplatky**.
    - Prodejní objednávky: Přejděte na **Pohledávky \> Nastavení \> Nastavení poplatků \> Automatické poplatky**.

1. V podokně seznamu v poli **Úroveň** vyberte úroveň, na kterou se vztahuje váš automatický poplatek:

    - *Hlavní* - použijte poplatky v záhlaví objednávky.
    - *Řádek* - použijte poplatky v řádcích objednávky.

1. Vyberte existující automatický poplatek a upravte jej, nebo vyberte **Nový** a definujte nový automatický poplatek.
1. V seznamu **Kód účtu** vyberte jednu z následujících hodnot a určete rozsah účtů, které budou ovlivněny:

    - *Tabulka* - Přiřaďte poplatky specifickému zákazníkovi nebo dodavateli.
    - *Skupina* - Přiřaďte poplatky skupině různých poplatků.
    - *Všechny* - Aplikuje náklady všem zákazníkům nebo dodavatelům.

1. V poli **Vztah zákazníků** nebo **Vztah dodavatelů** vyberte konkrétního zákazníka nebo dodavatele, pokud jste nastavili **Kód účtu** na *Tabulka*. Pokud jste pole **Kód účtu** nastavili na *Skupina*, vyberte zákazníka nebo skupinu poplatků dodavatele.
1. V poli **Kód položky** vyberte jednu z následujících hodnot a určete rozsah položek, které budou ovlivněny. Kód položky můžete vybrat pouze v případě, že definujete automatické poplatky na úrovni řádků.

    - *Tabulka* - Aplikuje poplatky specifické položce.
    - *Skupina* - Aplikuje poplatky skupině poplatků za položku.
    - *Všechny* - Aplikuje poplatky všem položkám.

1. V poli **Vztah položky** vyberte konkrétní položku, pokud jste nastavili pole **Kód položek** na *Tabulka*. Pokud nastavili pole **Kód položky** na *Skupina*, vyberte skupinu polatků položky.
1. **Pouze pro prodejní objednávky:** v poli **Kód způsobu doručení** vyberte jednu z následujících hodnot a určete rozsah režimů doručování, které budou ovlivněny:

    - *Tabulka* – Přiřazení poplatků ke konkrétnímu způsobu dodání.
    - *Skupina* – Přiřazení poplatků ke skupině způsobů dodání.
    - *Všechny* – Přiřazení poplatků ke všem způsobům dodání.

1. **Pouze pro prodejní objednávky**: v poli **Vztah způsobu doručení** vyberte konkrétní způsob doručení, pokud nastavíte pole **Kód způsobu doručení** na *Tabulka*. Vyberete-li pole **Kód způsobu doručení** na *Skupina*, vyberte skupinu způsobu doručení.
1. Na pevné záložce **Řádky** definujte poplatky a sazby poplatků, které budou použity při použití aktuálních automatických poplatků. Pomocí panelu nástrojů na této pevné záložce můžete přidat tolik řádků, kolik potřebujete. U každého řádku je třeba nastavit tato pole:

    - **Měna** - Vyberte měnu, která by měla být použita pro výpočet poplatku.
    - **Kód poplatku** - vyberte kód poplatku.
    - **Kategorie** - vyberte jednu z následujících hodnot:

        - *Fixní* – poplatky se zadávají jako pevná částka na řádku. Pevné náklady lze použít jako náklady v záhlaví objednávky i na řádcích objednávky.
        - *Ks* – Poplatek je založen na jednotce. Tyto poplatky lze použít pouze u řádků objednávek. Objeví se při výpočtu součtu objednávky.
        - *Procento* – Poplatky se zadávají jako procento na řádku. Procentní poplatky lze použít jako náklady v záhlaví objednávky i na řádcích objednávky.
        - *Mezipodnikové procento* - Poplatek se zadává jako procento na řádku pro mezipodnikové objednávky. Mezipodnikové procentní poplatky lze použít pouze u řádků objednávek.
        - *Externí* – poplatky se vypočítají pomocí služby třetí strany, která je přidružena k jednomu nebo více dopravců.

    - **Hodnota poplatků** - Zadejte hodnotu poplatku na základě kategorie, kterou jste vybrali.
    - **Kód měny poplatku** - Určete měnu poplatku, pokud chcete použít jinou měnu, než je měna uvedená v poli **Měna**. Jinou měnu lze zadat pouze, pokud je pole **Typ debetu** nebo **Typ kreditu** je nastaveno na *Účet hlavní knihy* nebo *Položka* pro vybraný kód poplatku.
    - **Od částky** - Zadejte počáteční částku pro použití automatických poplatků. V tomto kontextu odkazuje částka na celkovou výši objednávky.
    - **Po částku** - Zadejte konečnou částku pro použití automatických poplatků. V tomto kontextu odkazuje částka na celkovou výši objednávky.
    - **Skupina DPH** - Určete skupinu DPH.
    - **Web** a **Sklad** - Určete web a sklad, pokud by měly být poplatky účtovány pouze za konkrétní web a sklad.
    - **Ponechat** - zaškrtněte toto pole, chcete-li ponechat transakce poplatků po dokončení fakturace, aby se náklady použily pokaždé, když vytvoříte novou fakturu pro vybraný účet odběratele.

1. **Pouze pro prodejní objednávky:** Pokud chcete vypočítat vrstvené poplatky, viz [Vrstvené poplatky za prodejní objednávky](/dynamicsax-2012/appuser-itpro/about-tiered-charges-on-sales-orders) pro informaci.

## <a name="allocate-charges-from-the-header-to-a-line"></a>Přiřaďte poplatky ze záhlaví k řádku

Následující postup ukazuje, jak alokovat poplatky na úrovni záhlaví řádku. Před zahájením tohoto postupu byste již měli mít poplatek na úrovni záhlaví typu *pevná částka* a objednávky, kde je tento poplatek účtován. Objednávka by navíc již měla obsahovat alespoň jednu řádkovou položku.

1. Otevřete nákupní objednávku nebo objednávku poplatků.
1. V podokně Akce proveďte jeden z následujících kroků:

    - Pro nákupní objednávky: Na kartě **Nákup** ve skupině **Poplatky** vyberte **Přidělit poplatky**.
    - Pro prodejní objednávky: Na kartě **Prodej** ve skupině **Poplatky** vyberte **Přidělit poplatky**.

1. V dialogovém okně **Přiřaďte poplatky řádkům objednávky** nastavte následující pole:

    - **Přidělení poplatků** - Vyberte jednu z následujících hodnot a určete, jak mají být poplatky přiřazeny:

        - *Čistá částka* - Rozdělte poplatky podle jednotlivých částek v poměru k celkové čisté částce.
        - *Množství* - Rozdělte poplatky podle počtu jednotek pro každou linku v poměru k celkovému počtu jednotek.
        - *Na řádek* – náklady se přidělují stejnoměrně podle celkového počtu řádků.

    - **Přidělit poplatky řádkům** - Vyberte hodnotu a určete, zda mají být poplatky přiřazeny všem řádkům, pouze kladným řádkům nebo pouze záporným řádkům.
    - **Přidělit vše** - Toto políčko zaškrtněte, chcete-li přidělit náklady řádkům objednávky, i když má kód poplatků jiný typ debetu než *Položka*.
    - **Obdrženo** - Toto políčko zaškrtněte, chcete-li přidělit náklady jen přijatým řádkům objednávky.
    - **Na skladě** - Toto políčko zaškrtněte, chcete-li přidělit náklady jen řádkům objednávky na skladě.
    - **Zobrazit výběry a vymazat konkrétní řádky** - Zaškrtněte toto políčko, chcete-li z tohoto přidělení vyloučit konkrétní řádky. Pokud zaškrtnete toto políčko, otevře se mřížka **Vyberte řádky, které chcete vyloučit z alokace**. Tato mřížka obsahuje pouze řádky, které odpovídají kritériím definovaným v nastavení **Přidělit náklady k řádkům** a **Na skladě**. Například pokud nastavíte pole **Přidělit náklady k řádkům** na *Kladné řádky* a zaškrtnete možnost **Na skladě**, mřížka zobrazí pouze řádky, které jsou v kladné a na skladě. Kromě toho mřížka automaticky odfiltruje všechny řádky, pro které již bylo přijato celé množství. Když je mřížka otevřená, zrušte zaškrtnutí políčka **Zahrnout** pro každý řádek, který by měl být vyloučen z alokace. 

        > [!IMPORTANT]
        > Když pracujete s mřížkou **Vyberte řádky, které chcete vyloučit z alokace**, ponechte mřížku otevřenou, dokud nevyberete **Přidělit**. Pokud zavřete mřížku před výběrem **Přidělit**, vaše nastavení v mřížce budou ztracena. Proto budou poplatky přidělovány na základě kritérií, která jste dříve definovali.

1. Vyberte **Přidělit**, pokud chcete použít své nastavení a zavřete dialogové okno.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
