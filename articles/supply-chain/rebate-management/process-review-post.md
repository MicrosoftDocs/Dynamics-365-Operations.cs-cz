---
title: Zpracování, kontrola a zaúčtování rabatu
description: Tento článek popisuje, jak zpracovat vaše nabídky správy rabatu, vypočítat jejich slevy, zkontrolovat generované transakce, zaúčtovat transakce a zkontrolovat zaúčtování.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateDeal
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e63f02e5e93ec2ce8c321a20c2a0c5886edcbe42
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901930"
---
# <a name="process-review-and-post-rebates"></a>Zpracování, kontrola a zaúčtování rabatu

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak zpracovat vaše nabídky správy rabatu, vypočítat jejich slevy, zkontrolovat generované transakce, zaúčtovat transakce a zkontrolovat zaúčtování.

## <a name="change-the-status-of-a-deal"></a>Změna stavu nabídky

Každé nabídce můžete přiřadit stav, abyste ji mohli sledovat. Stav je pouze informační.

1. Vyberte nabídku (například na [stránce **Všechny nabídky správy rabatu**](rebate-management-deals.md)).
1. V podokně akcí na kartě **Nabídky správy rabatu** ve skupině **Udržovat** vyberte **Změnit stav**.
1. V dialogovém okně **Změnit stav** nastavte pole **Stav rabatu** do nového stavu.
1. Vyberte **OK**.

## <a name="calculate-fifo-purchase-prices"></a>Výpočet nákupních cen FIFO

Periodická úloha **Vypočítat nákupní cenu FIFO** pro výpočet rabatů musí být spuštěn pro [nabídky](rebate-management-deals.md), kde je pole **Základ ceny** nastaveno na *FIFO*. Systém použije k výpočtu hodnoty prodaného skladu pravidlo „první dovnitř, první ven“ (FIFO). Tato hodnota se poté použije k výpočtu rabatů dodavatele.

Přejděte na **Správa rabatu \> Periodické úkoly \> Vypočítat nákupní cenu FIFO**. V zobrazeném dialogovém okně vyberte **OK** a spusťte výpočet.

## <a name="create-source-transactions"></a>Vytváření zdrojových transakcí

Prodejní nebo nákupní objednávky, které mají zdrojové transakce, můžete vytvořit před nebo po vytvoření příslušné nabídky správy rabatu.

Každý řádek nabídky můžete nastavit tak, aby automaticky vytvořil zřízení rabatu zaúčtováním dodávky nebo faktury pro prodejní či nákupní objednávku. Pole **Typ transakce** pro řádek nabídky nastavte na *Dodávka* nebo *Faktura*, a možnost **Zpracování při zaúčtování** nastavte na *Ano*. Pokud je pole **Typ transakce** nastaveno na *Objednávka*, zpracování při zaúčtování je zakázáno. U zdrojových transakcí, které byly vytvořeny po aktivaci nabídky, můžete stále zpracovávat zřízení dle popisu v části [Zpracování nabídek správy rabatu](#process-deals) dále v tomto článku.

### <a name="enable-price-details"></a>Povolit podrobnosti o ceně

Než budete moci vytvářet zdrojové transakce, musíte zapnout možnost **Povolit podrobnosti o ceně** pro pohledávky.

1. Přejděte do **Pohledávky \> Nastavení \> Parametry pohledávek**.
1. Na kartě **Ceny** na záložce **Podrobnosti o ceně** nastavte možnost **Povolit podrobnosti o ceně** na *Ano*.

### <a name="create-a-source-transaction"></a>Vytvoření zdrojové transakce

Při vytváření zdrojové transakce postupujte takto:

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. Zvolte **Nové**.

    K napodobení způsobu generování nároků na rabat musíte nyní vytvořit prodejní objednávku, kde produkt a množství zajistí danému odběrateli nárok na rabat.

1. V poli **Účet zákazníka** zadejte nebo vyberte zákazníka, který bude mít nárok na rabat.
1. Výběrem **OK** vytvořte prodejní objednávku.
1. Na záložce **Řádky prodejní objednávky** přidejte řádek a nastavte jeho následující pole:

    - **Číslo položky** – Zadejte položku, na kterou se vztahuje rabat.
    - **Množství** – Zadejte množství, které je způsobilé pro nabídku rabatu, zahrnující řádek, kde je pole **Základ** nastaveno na *Množství*.
    - **Jednotková cena** – Zadejte cenu, které je způsobilé pro nabídku rabatu, zahrnující řádek, kde je pole **Základ** nastaveno na *Hodnota*.
    - **Lokalita** - Vyberte místo, kde je produkt k dispozici a které splňuje podmínky pro nabídku rabatu.
    - **Sklad** - Vyberte sklad, kde je produkt k dispozici a který splňuje podmínky pro nabídku rabatu.

1. Na záložce **Řádky prodejní objednávky** v panelu nástrojů vyberte **Řádek prodejní objednávky \> Podrobnosti o ceně**. Tento příkaz je k dispozici, pouze pokud jste povolili podrobnosti o ceně, jak je popsáno v předchozí části.
1. Na stránce **Podrobnosti o ceně** vyberte záložku **Správa rabatu**. Na této záložce jsou uvedeny všechny nabídky správy rabatu, které platí pro aktuální řádek objednávky, a také zde je odhad částky rabatu v měně objednávky. Upozorňujeme, že částky jsou pouze odhady budoucích nároků na rabat. Skutečné částky rabatu se mohou lišit. Zde uvádíme některé faktory, které mohou ovlivnit skutečné částky:

    - Celkový objem prodeje, kterého zákazník dosáhl na základě periodické smlouvy o rabatu.
    - Zda zákazník vrátil celá nebo částečná množství.
    - Zda příslušná prodejní objednávka dosáhla typu transakce (*Objednávka, dodání* nebo *Faktura*), který je definován pro nabídku správy rabatu.
    - Hodnota **Výstup** nabídky. Prázdná částka rabatu se zobrazí u dohod, kde je pole **Výstup** nastaveno na *Položka*.

1. Na záložce **Detail** si všimněte, že část **Odhad marže** obsahuje následující pole. Tato pole přidává správa rabatu. Všechna pole zobrazují hodnoty na jednotku (zatímco pole na záložce **Správa rabatu** zobrazují celkové hodnoty pro řádek).

    - **Částka rabatu správy rabatu** (pouze prodejní objednávky)
    - **Částka licenčního poplatku správy rabatu** (pouze prodejní objednávky)
    - **Částka rabatu dodavatele správy slevy** (prodejní objednávky a nákupní objednávky)

1. Zavřete stránku **Podrobnosti o ceně**.
1. Pokud by prodejní objednávka neměla nárok na rabaty, které jste si právě prohlíželi, podle následujících kroků rabaty vyřaďte. (Rabaty se však obvykle nevyřazují.)

    1. Na záložce **Řádky prodejní objednávky** vyberte relevantní řádek.
    1. Na záložce **Podrobnosti řádku** na kartě **Cena a sleva** nastavte možnost **Vyloučit ze správy rabatu** na *Ano*. Tato možnost se nevztahuje na nákupní objednávky. Dále platí, že když je tato možnost nastavena na *Ano*, jsou vyloučeny pouze rabaty pro zákazníky. Rabaty licenčních poplatků pro zákazníky a rabaty pro prodejce stále platí.

1. V podokně akcí na kartě **Vyskladnit a zabalit** ve skupině **Generovat** vyberte **Zaúčtovat dodací list**.
1. Na záložce **Parametry** v poli **Množství** vyberte *Vše*.
1. Vyberte **OK**.
1. Po zobrazení výzvy k potvrzení operace vyberte **OK**.
1. V podokně akcí na kartě **Faktura** ve skupině **Generovat** zvolte **Faktura**.
1. Na záložce **Parametry** v poli **Množství** vyberte *Vše* nebo *Dodací list*.
1. Vyberte **OK**.
1. Po zobrazení výzvy k potvrzení operace vyberte **OK**.

## <a name="process-rebate-management-deals"></a><a name="process-deals"></a>Zpracování nabídek správy rabatu

Když zpracováváte nabídku, systém vypočítá všechny příslušné rabaty a autorské poplatky, které jsou nastaveny. Pouze vybrané nabídky, které mají období výpočtu, jsou připravena k výpočtu a mají stav *Aktivní* budou zpracovány. Po dokončení zpracování systém vygeneruje sadu transakcí, které můžete zkontrolovat a poté zaúčtovat.

> [!NOTE]
> Ve všech případech jsou rabaty zpracovávány na úrovni, kterou stanoví nastavení každé nabídky **Odsouhlasit podle** (*Nabídka* nebo *Řádek*). Jednořádkové výpočty můžete provádět pouze u nabídek, kde je pole **Odsouhlasit podle** nastaveno na *Řádek*.

### <a name="process-all-lines-for-one-or-more-deals"></a>Zpracování všech řádků pro jednu nebo více nabídek

1. Otevřete příslušnou [stránku se seznamem nabídek rabatu](rebate-management-deals.md) pro typ nabídky, se kterým chcete pracovat.
1. Vyberte řádek pro každou nabídku, kterou chcete zpracovat (nebo otevřete nabídku, kterou chcete zpracovat).
1. V podokně akcí na kartě **Nabídky správy rabatu** ve skupině **Generovat** vyberte jeden z následujících příkazů:

    - **Zpracovat \> Zřízení** - Zřiďte sadu časových rozlišení pro každou relevantní nabídku rabatu, ale nezaúčtujte je. Tato položka nabídky není k dispozici pro nabídky, kde je pole **Výstup rabatu** nastaveno na *Položka*.
    - **Zpracovat \> Správa rabatu** - Zpracujte řadu transakcí, které poskytují hodnotu rabatu pro každou nabídku.
    - **Proces \> Odepsat** - U každé zdrojové transakce pro slevovou nabídku a stanovené období zpracujte rozptyl mezi částkami, které byly zaúčtovány pro zřízení a pro správu slev. Tato položka nabídky není k dispozici pro nabídky, kde je pole **Výstup rabatu** nastaveno na *Položka*.

1. V zobrazeném dialogovém okně nastavte pole **Od data** a **Do data** k definování časového období pro výpočet.
1. Tlačítkem **OK** spustíte výpočet.

### <a name="process-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Zpracujte jeden nebo více konkrétních řádků nabídky pro vybranou nabídku

1. Otevřete příslušnou [stránku se seznamem nabídek rabatu](rebate-management-deals.md) pro typ nabídky, se kterým chcete pracovat.
1. Otevřete nabídku, ze které chcete zpracovat řádek.
1. Vyberte kartu **Řádky** v pravém horním rohu.
1. Na záložce s náhledem **Správa rabatu** vyberte řádek pro každý řádek nabídky, který chcete zpracovat.
1. Na panelu nástrojů záložky s náhledem **Správa rabatu** vyberte jeden z následujících příkazů. (Tyto příkazy jsou k dispozici pouze pro nabídky, kde je pole **Odsouhlasit podle** nastaveno na *Řádek*.)

    - **Zpracovat \> Zřízení** - Zřiďte sadu časových rozlišení pro každý relevantní řádek nabídky, ale nezaúčtujte je. Tato položka nabídky není k dispozici pro nabídky, kde je pole **Výstup rabatu** nastaveno na *Položka*.
    - **Zpracovat \> Správa rabatu** - Zpracujte řadu transakcí, které poskytují hodnotu rabatu pro každý řádek nabídky.
    - **Proces \> Odepsat** - U každé zdrojové transakce pro slevovou nabídku a stanovené období zpracujte rozptyl mezi částkami, které byly zaúčtovány pro zřízení a pro správu slev. Tato položka nabídky není k dispozici pro nabídky, kde je pole **Výstup rabatu** nastaveno na *Položka*. 

1. V zobrazeném dialogovém okně nastavte pole **Od data** a **Do data** k definování časového období pro výpočet.
1. Tlačítkem **OK** spustíte výpočet.

### <a name="process-deals-using-a-batch-job"></a>Zpracování nabídek pomocí dávkové úlohy

Místo zpracování konkrétních nabídek nebo řádků nabídek můžete spustit dávkovou úlohu a zpracovat několik nabídek současně. Můžete volitelně použít filtry záznamů anebo nastavit opakující se plán. Chcete-li zpracovat nabídky pomocí dávkové úlohy, postupujte takto.

1. Proveďte jeden z následujících kroků:

    - Přejděte na **Správa rabatu \> Periodické úkoly \> Zpracovat \> Zřízení** a zřiďte sadu časového rozlišení pro každou příslušnou nabídku, ale bez jejich zaúčtování.
    - Přejděte na **Správa rabatu \> Periodické úkoly \> Zpracovat \> Správa rabatu** a zpracujte řadu transakcí, které poskytují hodnotu rabatu pro každou nabídku.
    - Přejděte na **Správa slev \> Periodické úkoly \> Zpracovat \> Odepsat** a stornujte dříve zaúčtované transakce a odepište je tak, aby bylo možné vypočítat nové transakce nabídek rabatu.

1. V zobrazeném dialogovém okně na záložce s náhledem **Parametry** v části **Období** nastavte pole **Od data** a **Do data** pro definování časového období transakcí pro výpočet.
1. V sekci **Období záruky** nastavte pole **Od data** a **Do data** k definování časového období pro výpočet.
1. Na záložce s náhledem **Záznamy, které mají být zahrnuty** můžete nastavit filtry k omezení sady nabídek, které bude dávková úloha zpracovávat. Tato nastavení fungují stejným způsobem, jako pro jiné typy dávkových úloh.
1. Na záložce s náhledem **Spustit na pozadí** můžete dle potřeby nastavit možnosti dávkového zpracování a plánování. Tato nastavení fungují stejným způsobem, jako pro jiné typy dávkových úloh.
1. Výběrem **OK** spusťte anebo naplánujte výpočet.

### <a name="process-deals-by-using-the-rebate-workbench"></a>Zpracování nabídek pomocí pracovní plochy pro rabat

Místo zpracování konkrétních nabídek nebo řádků nabídek můžete použít *pracovní plochu pro rabat* a zpracovat několik nabídek současně. Můžete volitelně použít filtry záznamů anebo nastavit opakující se plán. Nemusíte vybrat žádné řádky. Systém zpracuje všechny řádky, které splňují požadavky kalendářního data a filtru, které jste nastavili.

Chcete-li zpracovat nabídky pomocí pracovní plochy pro rabat, postupujte takto.

1. Přejděte do nabídky **Správa rabatu \> Nabídky správy rabatu \> Pracovní plocha pro rabat**.
1. V podokně akcí na kartě **Pracovní plocha pro rabat** ve skupině **Zpracování** vyberte jeden z následujících příkazů:

    - **Zpracovat \> Zřízení** – Zřiďte sadu časových rozlišení pro každý relevantní řádek nabídky, ale nezaúčtujte je.
    - **Zpracovat \> Správa rabatu** - Zpracujte řadu transakcí, které poskytují hodnotu rabatu pro každý řádek nabídky.
    - **Proces \> Odepsat** - U každé zdrojové transakce zpracujte rozptyl mezi zřízením a správou rabatu, které jsou zaúčtovány pro slevovou nabídku a stanovené období.

1. V dialogovém okně **Správa rabatu** v části **Období** nastavte pole **Od data** a **Do data** pro definování časového období výpočtu.
1. V sekci **Období záruky** nastavte pole **Od data** a **Do data** k definování časového období pro výpočet.
1. Na záložce s náhledem **Záznamy, které mají být zahrnuty** můžete nastavit filtry k omezení sady nabídek, které bude dávková úloha zpracovávat. Tato nastavení fungují stejným způsobem, jako pro jiné typy dávkových úloh.
1. Na záložce s náhledem **Spustit na pozadí** můžete dle potřeby nastavit možnosti dávkového zpracování a plánování. Tato nastavení fungují stejným způsobem, jako pro jiné typy dávkových úloh.
1. Výběrem **OK** spusťte anebo naplánujte výpočet.

## <a name="view-and-edit-rebate-management-transactions"></a>Zobrazení a úprava transakcí správy rabatu

Když zpracováváte jednu nebo více nabídek, systém vytvoří transakce, které můžete zobrazit a případně upravit před jejich zaúčtováním.

### <a name="view-and-edit-rebate-management-transactions-by-using-the-rebate-deals-list-page"></a>Prohlížení a úprava transakcí správy rabatu pomocí stránky seznamu nabídek rabatu

Chcete-li prohlížet a upravovat transakce správy rabatu pomocí stránky seznamu nabídek rabatu, postupujte následujícím způsobem.

1. Proveďte jeden z následujících kroků:

    - Vyberte nabídku, pro kterou chcete zobrazit transakce (například na [stránce **Všechny nabídky správy rabatu**](rebate-management-deals.md)). V podokně akcí na kartě **Nabídky správy rabatu** ve skupině **Transakce** vyberte **Transakce** nebo **Transakce záruky**, v závislosti na typu transakce, kterou chcete zobrazit.
    - Otevřete nabídku (například na [stránce **Všechny nabídky správy rabatu**](rebate-management-deals.md)) pro zobrazení jejích podrobností. Na záložce s náhledem **Správa rabatu** vyberte řádek nabídky, pro který chcete zobrazit transakce. Poté na panelu nástrojů vyberte **Transakce** nebo **Transakce záruky**, v závislosti na typu transakce, kterou chcete zobrazit. (Tato tlačítka jsou k dispozici pouze pro nabídky, kde je pole **Odsouhlasit podle** nastaveno na *Řádek*.)

1. Zobrazí se stránka **Transakce data správy rabatu** nebo **Transakce záruky správy rabatu**. Obsahuje mřížku, kde každý řádek představuje kolekci transakcí z jednoho období rabatu nebo záruky. Vyberte řádek v mřížce a poté v podokně akcí vyberte **Zdrojové transakce** pro zobrazení transakcí, které patří do daného řádku.
1. Stránka, která se zobrazí, obsahuje seznam transakcí vybraného typu, které patří do vybraného řádku. Každá transakce poskytuje relevantní podrobnosti v závislosti na typu transakce. U transakcí záruky můžete zobrazit pouze seznam. U ostatních typů transakcí můžete na této stránce provést následující akce:

    - Chcete-li ověřit celkovou hodnotu všech nárokovaných transakcí na stránce, podívejte se na pole **Nárokovaná částka**.
    - Chcete-li zobrazit další informace o jakékoli transakci, vyberte ji a poté vyberte kartu **Obecné**, **Finanční dimenze** nebo **Dimenze**.
    - Chcete-li zobrazit případná použitelná snížení, vyberte v podokně akcí **Transakce snížení**. Další informace viz [Zásady snižování rabatu](rebate-reduction-principle.md).
    - Chcete-li označit transakce jako nárokované nebo nenárokované, pokud používáte proces nároků, vyberte příslušné řádky a poté v podokně akcí vyberte jeden z následujících příkazů. (Procesy nároku povolíte na [stránce **Parametry správy rabatu**](rebate-management-parameters.md) .)

        - **Nastavit nárokované \> Vše** - Označte všechny transakce jako nárokované.
        - **Nastavit nárokované \> Vybrané** - Označte vybrané transakce jako nárokované.
        - **Nastavit nenárokované \> Vše** - Označte všechny transakce jako nenárokované.
        - **Nastavit nenárokované \> Vybrané** - Označte vybrané transakce jako nenárokované.

    - Vyberte **Zaúčtovat** v podokně akcí pro zaúčtování pohledávek ze všech příslušných řádků. Pokud používáte proces nároků (když je volba **Použijte proces nároků** povolena na stránce **Parametry správy rabatu**), pouze řádky označené jako **Nárokováno** jsou zaúčtovány. Jinak se zaúčtují všechny zdrojové transakce pro vybranou transakci rabatu. Tlačítko **Zaúčtovat** je k dispozici pouze u transakcí rabatu. Není k dispozici pro transakce zřízení a odpisů. V dialogovém okně **Zaúčtovat** se automaticky nastaví pole **Od data** a **Do data**. Nastavte pole **Datum zaúčtování** a poté zvolte **OK**.
    - Chcete-li upravit částku, která se zobrazuje u jakékoli otevřené nebo nezaúčtované transakce, vyberte transakci a postupujte podle jednoho z těchto kroků:

        - Upravte hodnotu v poli **Opravená částka**.
        - V podokně akcí zvolte **Nastavit opravu**. Poté v zobrazeném rozevíracím dialogovém okně v poli **Opravená částka** zadejte hodnotu.

> [!NOTE]
> Pokud používáte proces nároků , když zpracováváte další období, seznam transakcí bude zahrnovat všechny nenárokované transakce z předchozího zaúčtování, plus všechny nové transakce za vybrané období.

### <a name="view-and-edit-rebate-management-transactions-by-using-the-rebate-workbench"></a>Prohlížení a úprava transakcí správy rabatu pomocí pracovní plochy pro rabat

Chcete-li prohlížet a upravovat transakce správy rabatu pomocí pracovní plochy pro rabat, postupujte následujícím způsobem.

1. Přejděte do nabídky **Správa rabatu \> Nabídky správy rabatu \> Pracovní plocha pro rabat**.
1. Nastavte pole **Zobrazit** na *Nezaúčtováno*.
1. Stránka **Pracovní plocha pro rabat** zobrazuje seznam transakcí. Každá transakce poskytuje relevantní podrobnosti. Tyto podrobnosti se liší v závislosti na typu transakce. Na této stránce můžete provést následující akce:

    - Chcete-li zobrazit další informace o jakékoli transakci, vyberte ji a poté vyberte kartu **Obecné**, **Finanční dimenze** nebo **Dimenze**.
    - Pokud používáte proces nároku, můžete transakce označit jako nárokované nebo nenárokované. Vyberte relevantní řádky a poté v podokně akcí na kartě **Pracovní plocha pro rabat** vyberte jeden z následujících příkazů. (Procesy nároku povolíte na stránce [**Parametry správy rabatu**](rebate-management-parameters.md).)

        - **Nastavit nárokované** – Označte vybrané transakce jako nárokované.
        - **Nastavit nenárokované** – Označte vybrané transakce jako nenárokované.

    - Chcete-li zaúčtovat nárok na jeden nebo více řádků, vyberte příslušné řádky. Poté v podokně akcí na kartě **Pracovní plocha pro rabat** zvolte **Zaúčtovat**. Tlačítko **Zaúčtovat** je k dispozici pro zřizovací, rabatové a odpisové transakce. V dialogovém okně **Zaúčtovat** se automaticky nastaví pole **Od data** a **Do data**. Nastavte pole **Datum zaúčtování** a poté zvolte **OK**.
    - Chcete-li upravit částku, která se zobrazuje u jakékoli otevřené nebo nezaúčtované transakce, vyberte transakci a postupujte podle jednoho z těchto kroků:

        - Upravte hodnotu v poli **Opravená částka**.
        - V podokně akcí na kartě **Pracovní plocha pro rabat** zvolte **Nastavit opravu**. Poté v zobrazeném rozevíracím dialogovém okně v poli **Opravená částka** zadejte hodnotu.

> [!NOTE]
> Pokud používáte proces nároků , když zpracováváte další období, seznam transakcí bude zahrnovat všechny nenárokované transakce z předchozího zaúčtování, plus všechny nové transakce za vybrané období.

## <a name="post-rebates-transactions"></a>Zaúčtování transakcí rabatu

Chcete-li zaúčtovat hodnotu zpracovaného zřízení, částku správy rabatu a odpis, musíte spustit proces účtování. Proces zaúčtování označí transakce zřízení, správy rabatu nebo odpisy jako zaúčtované a vytvoří cílovou transakci. Pokud nemusíte kontrolovat cílovou transakci, lze tyto transakce nastavit tak, aby byly automaticky zaúčtovány.

### <a name="set-up-the-system-to-post-all-target-transactions-automatically"></a>Nastavení systému pro automatické zaúčtování všech cílových transakcí

Chcete-li nastavit systém tak, aby zaúčtoval všechny cílové transakce, jakmile budou vygenerovány zaúčtováním zřízení, částky správy rabatu nebo odpisem, zapněte možnosti **Automaticky zaúčtovat deníky** anebo **Automaticky zaúčtovat faktury s volným textem** na stránce **Parametry správy rabatu**. Další informace naleznete v tématu [Parametry správy rabatu](rebate-management-parameters.md).

### <a name="post-transactions-for-all-lines-for-one-or-more-deals"></a>Zaúčtování transakcí pro všechny řádky pro jednu nebo více nabídek

Po zpracování příslušných nabídek postupujte podle těchto kroků a zkontrolujte a zaúčtujte vygenerované transakce pro všechny řádky pro jednu nebo více nabídek.

1. Otevřete příslušnou [stránku se seznamem nabídek rabatu](rebate-management-deals.md) pro typ nabídky, se kterým chcete pracovat.
1. Vyberte řádek pro každou nabídku, kterou chcete zaúčtovat (nebo otevřete nabídku, kterou chcete zaúčtovat).
1. V podokně akcí na kartě **Nabídky správy rabatu** ve skupině **Generovat** vyberte jeden z následujících příkazů:

    - **Zaúčtovat \> Zřízení** - Zaúčtujte dostupné transakce časového rozlišení, které jste vytvořili.
    - **Zaúčtovat \> Správa rabatu** - Zaúčtujte dostupné transakce rabatu, které jste vytvořili.
    - **Zaúčtovat \> Odepsat** - Zaúčtujte dostupné transakce odpisu, které jste vytvořili.

1. V zobrazeném dialogovém okně nastavte pole **Datum zaúčtování**. Poté nastavte pole **Od data** a **Do data** k definování časového období pro transakce, které musí být zaúčtovány.
1. Výběrem tlačítka **OK** zaúčtujte transakce.

### <a name="post-transactions-for-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Zaúčtování transakcí pro jeden nebo více konkrétních řádků nabídky pro vybranou nabídku

Po zpracování příslušných nabídek postupujte podle těchto kroků a zkontrolujte a zaúčtujte vygenerované transakce pro více konkrétních řádků nabídky pro vybranou nabídku. Tuto proceduru lte použít pouze pro nabídky, kde je pole **Odsouhlasit podle** nastaveno na *Řádek*.

1. Otevřete příslušnou [stránku se seznamem nabídek rabatu](rebate-management-deals.md) pro typ nabídky, se kterým chcete pracovat.
1. Otevřete obchod, který obsahuje řádek, pro který chcete zaúčtovat transakce.
1. Vyberte kartu **Řádky** v pravém horním rohu.
1. Na záložce s náhledem **Správa rabatu** vyberte řádek pro každý řádek nabídky, který chcete zaúčtovat.
1. Na panelu nástrojů záložky s náhledem **Správa rabatu** vyberte jeden z následujících příkazů. (Tyto příkazy jsou k dispozici pouze pro nabídky, kde je pole **Odsouhlasit podle** nastaveno na *Řádek*.)

    - **Zaúčtovat \> Zřízení** - Zaúčtujte dostupné transakce časového rozlišení, které jste vytvořili.
    - **Zaúčtovat \> Správa rabatu** - Zaúčtujte dostupné transakce rabatu, které jste vytvořili.
    - **Zaúčtovat \> Odepsat** - Zaúčtujte dostupné transakce odpisu, které jste vytvořili.

1. V zobrazeném dialogovém okně nastavte pole **Datum zaúčtování**. Poté nastavte pole **Od data** a **Do data** k definování časového období pro transakce, které musí být zaúčtovány.
1. Výběrem tlačítka **OK** zaúčtujte transakce.

### <a name="post-transactions-using-a-batch-job"></a>Zaúčtování transakcí pomocí dávkové úlohy

Místo zaúčtování transakcí pro konkrétní nabídky nebo řádků nabídek můžete spustit dávkovou úlohu pro zaúčtování transakcí pro několik nabídek současně. Můžete volitelně použít filtry záznamů anebo nastavit opakující se plán. Chcete-li zaúčtovat transakce pomocí dávkové úlohy, postupujte takto.

1. Proveďte jeden z následujících kroků:

    - Přejděte **Správa rabatu \> Periodické úkoly \> Zaúčtovat \> Zřízení** a zaúčtujte dostupné transakce časového rozlišení, které jste vytvořili.
    - Přejděte **Správa rabatu \> Periodické úkoly \> Zaúčtovat \> Správa rabatu** a zaúčtujte dostupné transakce rabatu, které jste vytvořili.
    - Přejděte **Správa rabatu \> Periodické úkoly \> Zaúčtovat \> Odepsat** a zaúčtujte dostupné transakce odpisu, které jste vytvořili.

1. V zobrazeném dialogovém okně na záložce s náhledem **Parametry** v sekci **Období** nastavte pole **Datum zaúčtování**. Poté nastavte pole **Od data** a **Do data** k definování časového období pro transakce, které musí být zaúčtovány.
1. V sekci **Období záruky** nastavte pole **Od data** a **Do data** k definování časového období pro záruky, které musí být zaúčtovány.
1. Na záložce s náhledem **Záznamy, které mají být zahrnuty** můžete nastavit filtry k omezení sady nabídek, které bude dávková úloha zpracovávat. Tato nastavení fungují stejným způsobem, jako pro jiné typy dávkových úloh.
1. Na záložce s náhledem **Spustit na pozadí** můžete dle potřeby nastavit možnosti dávkového zpracování a plánování. Tato nastavení fungují stejným způsobem, jako pro jiné typy dávkových úloh.
1. Výběrem **OK** spusťte anebo naplánujte výpočet.

### <a name="post-transactions-by-using-the-rebate-workbench"></a>Zaúčtování transakcí pomocí pracovní plochy pro rabat

Poté, co jste zpracovali transakce zřízení, rabatu nebo odpisu, podle dále uvedených kroků použijte pracovní plochu pro rabat ke kontrole a zaúčtování vygenerovaných transakcí pro jeden nebo více konkrétních řádků transakcí u všech nabídek.

1. Přejděte do nabídky **Správa rabatu \> Nabídky správy rabatu \> Pracovní plocha pro rabat**.
1. V mřížce zaškrtněte řádek u každého řádku transakce, kterou chcete zaúčtovat. Můžete vybrat nezaúčtované transakce zřízení, rabatu nebo odpisu. Platí následující pravidla:

    - Systém také zaúčtuje všechny řádky, které mají stejné **Číslo transakce rabatu** jako řádky, které vyberete.
    - Systém nezaúčtuje žádné řádky typu transakce *Rabat*, které nejsou označeny jako nárokované.
    - Pokud vyberete řádky, které již byly zaúčtovány, systém je přeskočí.
    - Tlačítko **Zaúčtovat** je k dispozici, pouze pokud vyberete alespoň jeden nezaúčtovaný řádek.

1. V podokně Akce na kartě **Pracovní plocha pro rabat** ve skupině **Zpracování** zvolte **Zaúčtovat**.
1. V dialogovém okně **Zaúčtovat** nastavte pole **Datum zaúčtování**. Pole **Od data** a **Do data** se nastaví automaticky podle nejstarší hodnoty **Od data** a nejnovější hodnoty **Do data** pro vybrané řádky.
1. Výběrem tlačítka **OK** zaúčtujte transakce.

## <a name="review-rebate-management-journals"></a><a name="review-journals"></a>Kontrola deníků správy rabatů

Po zaúčtování transakcí můžete zkontrolovat výsledné deníky, dokumenty nebo položky. Cílové transakce pro rabaty a autorské poplatky jsou založeny na typu platby, který je nastaven v účetním profilu, a typu výstupu rabaty. Například pokud je výstup rabatu nastaven na *Položka*, bude vytvořena prodejní objednávka pro rabat zákazníka a bude vytvořena nákupní objednávka pro rabat dodavatele. Tyto objednávky lze prohlížet prostřednictvím cílových transakcí. Pokud je platba nastavena na použití závazků, bude pro rabaty zákazníka vytvořena faktura dodavatele pro dodavatele, která je nastavena na zákazníka.

### <a name="review-journals-by-using-the-rebate-deals-list-page"></a>Kontrola deníků pomocí stránky se seznamem nabídek rabatu

Chcete-li zkontrolovat položky deníku, které jsou přidruženy k nabídce správy rabatů, postupujte takto.

1. Otevřete příslušnou [stránku se seznamem nabídek rabatu](rebate-management-deals.md) pro typ nabídky, se kterým chcete pracovat.
1. Vyberte dohodu, u které chcete zkontrolovat položky deníku.
1. V podokně akcí na kartě **Nabídky správy rabatu** ve skupině **Transakce** vyberte **Transakce** nebo **Transakce záruky**, v závislosti na typu transakce, kterou chcete zobrazit.
1. Nastavte pole **Zobrazit** na *Vše* nebo *Zaúčtováno*.
1. Najděte a vyberte kolekci transakcí, kterou chcete zkontrolovat, a poté v podokně akcí vyberte jedno z následujících tlačítek. (Tato tlačítka jsou k dispozici, pouze pokud existují relevantní zaúčtování pro vybranou kolekci transakcí.)

    - **Cílové transakce** - Zkontrolujte relevantní deníky a další typy dokumentů, které byly vygenerovány vybranou nabídkou.
    - **Položky** - Zkontrolujte relevantní prodejní objednávky nebo nákupní objednávky, které byly vygenerovány vybranou nabídkou.

1. Zobrazí se seznam příslušných deníků, dokumentů nebo položek. Chcete-li zobrazit více informací o jakémkoli deníku, dokumentu nebo položce, vyberte jeho řádek a poté v podokně akcí vyberte **Zobrazit podrobnosti**.

### <a name="review-journals-by-using-the-rebate-workbench"></a>Kontrola deníků pomocí pracovní plochy pro rabat

Chcete-li zkontrolovat deníky pomocí pracovní plochy pro rabat, postupujte takto.

1. Přejděte do nabídky **Správa rabatu \> Nabídky správy rabatu \> Pracovní plocha pro rabat**.
1. Nastavte pole **Zobrazit** na _Vše_ nebo _Zaúčtováno_.
1. Najděte a vyberte řádek, který chcete prozkoumat. Poté v podokně akcí na kartě **Pracovní plocha pro rabat** ve skupině **Zobrazit** zvolte **Cílové transakce**. Toto tlačítko je k dispozici pouze v případě, že pro vybraný řádek existují příslušná zaúčtování.
1. Zobrazí se seznam příslušných deníků, dokumentů nebo položek. Chcete-li zobrazit více informací o jakémkoli deníku, dokumentu nebo položce, vyberte jeho řádek a poté v podokně akcí vyberte **Zobrazit podrobnosti**.

## <a name="rebate-management-transactions-on-the-deduction-workbench"></a>Transakce správy rabatu na pracovní ploše odpočtu

Když zaúčtujete transakci správy rabatu, která má jednu z následujících hodnot **Způsob platby**, systém vytvoří deník pro odpočty zákazníků nebo fakturu s volným textem pro příslušný zákaznický účet:

- Srážky u odběratele
- Odpočty zákazníků daňové faktury
- Obchodní výdaje
- Vykazování

Jakmile je cílová transakce vytvořena a zaúčtována, bude k dispozici jako otevřená transakce na stránce **Pracovní plocha odpočtu** (**Prodej a marketing \> Obchodní náhrady \> Srážky \> Pracovní plocha odpočtu**). Otevřené transakce mají **Typ nároku** nastaven na *Správa rabatu* a hodnota **Číslo transakce rabatu** je k dispozici pro umožnění sledovatelnosti. Datum je nastaveno na datum zaúčtování cílové transakce správy rabatu. Chcete-li použít pracovní plochu odpočtu k vypořádání otevřených transakcí se stávajícími odpočty pro stejný zákaznický účet, vyberte příkaz **Udržovat \> Spárovat** v podokně akcí.

Další informace viz [Správa odpočtů pomocí pracovní plochy odpočtu](deduction-workbench.md).

## <a name="purge-unposted-transactions"></a>Vyčištění nezaúčtovaných transakcí

Poté, co zpracujete transakce zřízení, rabatu nebo odpisu, vymažte vybrané nezaúčtované transakce podle těchto pokynů.

1. Přejděte do nabídky **Správa rabatu \> Nabídky správy rabatu \> Pracovní plocha pro rabat**.
2. Nastavte pole **Zobrazit** na *Nezaúčtováno*.
3. Najděte a vyberte transakce, které chcete odstranit. Poté v podokně Akce na kartě **Pracovní plocha pro rabat** ve skupině **Zpracování** zvolte **Vyčistit**.
4. Výběrem tlačítka **OK** se nezaúčtované transakce odstraní.

## <a name="cancel-a-posted-provision"></a>Zrušení zaúčtovaného zřízení

Poté, co zpracujete a zaúčtujete zřízení, zrušíte transakce zaúčtovaného zřízení následujícím způsobem.

1. Přejděte do nabídky **Správa rabatu \> Nabídky správy rabatu \> Pracovní plocha pro rabat**.
2. Nastavte pole **Zobrazit** na *Zaúčtováno*.
3. Najděte a vyberte transakce zřízení, které chcete zrušit. Poté v podokně Akce na kartě **Pracovní plocha pro rabat** ve skupině **Zpracování** zvolte **Zrušit zřízení**.
4. Výběrem tlačítka **OK** změňte transakce.

Tato zrušení zřízení budou také viditelná v příslušných [denících pro správu slev](#review-journals).
