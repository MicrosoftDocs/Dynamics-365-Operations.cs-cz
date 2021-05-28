---
title: Zpracování, kontrola a zaúčtování rabatu
description: Toto téma popisuje, jak zpracovat vaše nabídky správy rabatu, vypočítat jejich slevy, zkontrolovat generované transakce, zaúčtovat transakce a zkontrolovat zaúčtování.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateDeal
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 5188fa271cd9eb24140a9edcf507a3da72b61074
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020524"
---
# <a name="process-review-and-post-rebates"></a>Zpracování, kontrola a zaúčtování rabatu

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak zpracovat vaše nabídky správy rabatu, vypočítat jejich slevy, zkontrolovat generované transakce, zaúčtovat transakce a zkontrolovat zaúčtování.

## <a name="change-the-status-of-a-deal"></a>Změna stavu nabídky

Každé nabídce můžete přiřadit stav, abyste ji mohli sledovat. Stav je pouze informační.

1. Vyberte nabídku (například na [stránce **Všechny nabídky správy rabatu**](rebate-management-deals.md)).
1. V podokně akcí na kartě **Nabídky správy rabatu** ve skupině **Udržovat** vyberte **Změnit stav**.
1. V dialogovém okně **Změnit stav** nastavte pole **Stav rabatu** do nového stavu.
1. Vyberte **OK**.

## <a name="calculate-fifo-purchase-prices"></a>Výpočet nákupních cen FIFO

Periodická úloha **Vypočítat nákupní cenu FIFO** pro výpočet rabatů musí být spuštěn pro [nabídky](rebate-management-deals.md), kde je pole **Základ ceny** nastaveno na *FIFO*. Systém použije k výpočtu hodnoty prodaného skladu pravidlo „první dovnitř, první ven“ (FIFO). Tato hodnota se poté použije k výpočtu rabatů dodavatele.

Přejděte na **Správa rabatu \> Periodické úkoly \> Vypočítat nákupní cenu FIFO**. V zobrazeném dialogovém okně vyberte **OK** a spusťte výpočet.

## <a name="process-rebate-management-deals"></a>Zpracování nabídek správy rabatu

Když zpracováváte nabídku, systém vypočítá všechny příslušné rabaty a autorské poplatky, které jsou nastaveny. Pouze vybrané nabídky, které mají období výpočtu, jsou připravena k výpočtu a mají stav *Aktivní* budou zpracovány. Po dokončení zpracování systém vygeneruje sadu transakcí, které můžete zkontrolovat a poté zaúčtovat.

> [!NOTE]
> Ve všech případech jsou rabaty zpracovávány na úrovni, kterou stanoví nastavení každé nabídky **Odsouhlasit podle** (*Nabídka* nebo *Řádek*). Jednořádkové výpočty můžete provádět pouze u nabídek, kde je pole **Odsouhlasit podle** nastaveno na *Řádek*.

### <a name="process-all-lines-for-one-or-more-deals"></a>Zpracování všech řádků pro jednu nebo více nabídek

1. Otevřete příslušnou [stránku se seznamem nabídek rabatu](rebate-management-deals.md) pro typ nabídky, se kterým chcete pracovat.
1. Vyberte řádek pro každou nabídku, kterou chcete zpracovat (nebo otevřete nabídku, kterou chcete zpracovat).
1. V podokně akcí na kartě **Nabídky správy rabatu** ve skupině **Generovat** vyberte jeden z následujících příkazů:

    - **Zpracovat \> Zřízení** - Zřiďte sadu časových rozlišení pro každou relevantní nabídku rabatu, ale nezaúčtujte je.
    - **Zpracovat \> Správa rabatu** - Zpracujte řadu transakcí, které poskytují hodnotu rabatu pro každou nabídku.
    - **Zpracovat \> Odepsat** - Stornujte dříve zaúčtované transakce a odepište je tak, aby bylo možné vypočítat nové transakce nabídek rabatu.

1. V zobrazeném dialogovém okně nastavte pole **Od data** a **Do data** k definování časového období pro výpočet.
1. Tlačítkem **OK** spustíte výpočet.

### <a name="process-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Zpracujte jeden nebo více konkrétních řádků nabídky pro vybranou nabídku

1. Otevřete příslušnou [stránku se seznamem nabídek rabatu](rebate-management-deals.md) pro typ nabídky, se kterým chcete pracovat.
1. Otevřete nabídku, ze které chcete zpracovat řádek.
1. Vyberte kartu **Řádky** v pravém horním rohu.
1. Na záložce s náhledem **Správa rabatu** vyberte řádek pro každý řádek nabídky, který chcete zpracovat.
1. Na panelu nástrojů záložky s náhledem **Správa rabatu** vyberte jeden z následujících příkazů. (Tyto příkazy jsou k dispozici pouze pro nabídky, kde je pole **Odsouhlasit podle** nastaveno na *Řádek*.)

    - **Zpracovat \> Zřízení** - Zřiďte sadu časových rozlišení pro každý relevantní řádek nabídky, ale nezaúčtujte je.
    - **Zpracovat \> Správa rabatu** - Zpracujte řadu transakcí, které poskytují hodnotu rabatu pro každý řádek nabídky.
    - **Zpracovat \> Odepsat** - Stornujte dříve zaúčtované transakce a odepište je tak, aby bylo možné vypočítat nové transakce nabídek rabatu.

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

## <a name="view-and-edit-rebate-management-transactions"></a>Zobrazení a úprava transakcí správy rabatu

Když zpracováváte jednu nebo více nabídek, systém vytvoří transakce, které můžete zobrazit a případně upravit před jejich zaúčtováním.

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

    - Chcete-li zaúčtovat nárok pro jeden nebo více řádků, vyberte příslušné řádky a poté v podokně akcí vyberte **Zaúčtovat**. (Tlačítko **Zaúčtovat** je k dispozici pouze u transakcí rabatu. Není k dispozici pro transakce zřízení a odpisů.) V dialogovém okně **Zaúčtovat** jsou pole **Od data** a **Do data** nastavena automaticky. Nastavte pole **Datum zaúčtování** a poté zvolte **OK**.
    - Chcete-li upravit částku, která se zobrazuje u jakékoli otevřené nebo nezaúčtované transakce, vyberte transakci a postupujte podle jednoho z těchto kroků:

        - Upravte hodnotu v poli **Opravená částka**.
        - V podokně akcí zvolte **Nastavit opravu**. Poté v zobrazeném rozevíracím dialogovém okně v poli **Opravená částka** zadejte hodnotu.

> [!NOTE]
> Když zpracováváte další období, seznam transakcí bude zahrnovat všechny nenárokované transakce z předchozího zaúčtování, plus všechny nové transakce za vybrané období.

## <a name="post-rebates-transactions"></a>Zaúčtování transakcí rabatu

Chcete-li zaúčtovat hodnotu rabatů a odpočtů, musíte spustit proces účtování, pokud jste nenastavili svůj systém tak, aby je zaúčtoval automaticky.

### <a name="set-up-the-system-to-post-all-transactions-automatically"></a>Nastavení systému pro automatické zaúčtování všech transakcí

Chcete-li nastavit systém tak, aby zaúčtoval všechny transakce, jakmile budou vygenerovány, zapněte možnosti **Automaticky zaúčtovat deníky** anebo **Automaticky zaúčtovat faktury s volným textem** na stránce **Parametry správy rabatu**. Další informace naleznete v tématu [Parametry správy rabatu](rebate-management-parameters.md).

### <a name="post-transactions-for-all-lines-for-one-or-more-deals"></a>Zaúčtování transakcí pro všechny řádky pro jednu nebo více nabídek

Pokud nepoužíváte automatické zaúčtování, po zpracování příslušných nabídek postupujte podle těchto kroků a zkontrolujte a zaúčtujte vygenerované transakce pro všechny řádky pro jednu nebo více nabídek.

1. Otevřete příslušnou [stránku se seznamem nabídek rabatu](rebate-management-deals.md) pro typ nabídky, se kterým chcete pracovat.
1. Vyberte řádek pro každou nabídku, kterou chcete zaúčtovat (nebo otevřete nabídku, kterou chcete zaúčtovat).
1. V podokně akcí na kartě **Nabídky správy rabatu** ve skupině **Generovat** vyberte jeden z následujících příkazů:

    - **Zaúčtovat \> Zřízení** - Zaúčtujte dostupné transakce časového rozlišení, které jste vytvořili.
    - **Zaúčtovat \> Správa rabatu** - Zaúčtujte dostupné transakce rabatu, které jste vytvořili.
    - **Zaúčtovat \> Odepsat** - Zaúčtujte dostupné transakce odpisu, které jste vytvořili.

1. V zobrazeném dialogovém okně nastavte pole **Datum zaúčtování**. Poté nastavte pole **Od data** a **Do data** k definování časového období pro transakce, které musí být zaúčtovány.
1. Výběrem tlačítka **OK** zaúčtujte transakce.

### <a name="post-transactions-for-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Zaúčtování transakcí pro jeden nebo více konkrétních řádků nabídky pro vybranou nabídku

Pokud nepoužíváte automatické zaúčtování, po zpracování příslušných nabídek postupujte podle těchto kroků a zkontrolujte a zaúčtujte vygenerované transakce pro jeden nebo více konkrétních řádků nabídky pro zvolenou nabídku.

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

## <a name="review-rebate-management-journals"></a>Kontrola deníků správy rabatů

Po zaúčtování transakcí můžete zkontrolovat výsledné deníky, dokumenty nebo položky. Cílové transakce pro rabaty a autorské poplatky jsou založeny na typu platby, který je nastaven v účetním profilu, a typu výstupu rabaty. Například pokud je výstup rabatu nastaven na *Položka*, bude vytvořena prodejní objednávka, kterou lze zobrazit prostřednictvím cílových transakcí. Pokud je platba nastavena na použití závazků, bude pro rabaty zákazníka vytvořena faktura dodavatele pro dodavatele, která je nastavena na zákazníka.

Chcete-li zkontrolovat položky deníku, které jsou přidruženy k nabídce správy rabatů, postupujte takto.

1. Otevřete příslušnou [stránku se seznamem nabídek rabatu](rebate-management-deals.md) pro typ nabídky, se kterým chcete pracovat.
1. Vyberte dohodu, u které chcete zkontrolovat položky deníku.
1. V podokně akcí na kartě **Nabídky správy rabatu** ve skupině **Transakce** vyberte **Transakce** nebo **Transakce rabatu**, v závislosti na typu transakce, kterou chcete zobrazit.
1. Ujistěte se, že pole **Ukázat** je nastaveno na *Vše* nebo *Zaúčtováno*.
1. Najděte a vyberte kolekci transakcí, kterou chcete zkontrolovat, a poté v podokně akcí vyberte jedno z následujících tlačítek. (Tato tlačítka jsou k dispozici, pouze pokud existují relevantní zaúčtování pro vybranou kolekci transakcí.)

    - **Cílové transakce** - Zkontrolujte relevantní deníky a další typy dokumentů, které byly vygenerovány vybranou nabídkou.
    - **Položky** - Zkontrolujte relevantní položky, které byly vygenerovány vybranou nabídkou.

1. Zobrazí se seznam příslušných deníků, dokumentů nebo položek. Chcete-li zobrazit více informací o jakémkoli deníku, dokumentu nebo položce, vyberte jeho řádek a poté v podokně akcí vyberte **Zobrazit podrobnosti**.
