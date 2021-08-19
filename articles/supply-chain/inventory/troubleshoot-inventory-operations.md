---
title: Řešení potíží se skladovými operacemi
description: Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci se skladovými operacemi.
author: sherry-zheng
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 1198bc12830afa2ae2c5eb8e77413a9d8ef70c625823f676ab1965ff250c2443
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730381"
---
# <a name="troubleshoot-inventory-operations"></a>Řešení potíží se skladovými operacemi

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci se skladovými operacemi.

## <a name="i-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a>Nemohu najít rozevírací dialogové okno „Pracovní postup“ pro deníky zásob.

### <a name="issue-description"></a>Popis problému

Nemůžete najít rozevírací dialogové okno **Workflow** na stránce deníku nebo související operace pracovního postupu nejsou k dispozici.

K tomuto problému může dojít ze tří důvodů, jak je popsáno v následujících podsekcích.

### <a name="issue-resolution-1"></a>Řešení problému 1

Pokud se problém týká všech uživatelů, může docházet k tomu, že pracovnímu postupu schválení nebyl přiřazen název deníku. Chcete-li opravit problém, postupujte následovně.

1. Přejděte na **Řízení zásob &gt; Nastavení &gt; Názvy deníků &gt; Zásoby**.
1. V podokně seznamu vyberte ze sloupce seznamu název deníku.
1. Na pevné záložce **Obecné** nastavte možnost **workflow schválení** na *Ano*. Vyberte **Ano** po zobrazení výzvy k potvrzení změny.
1. V poli **Workflow** vyberte workflow, který chcete použít pro vybraný název deníku.

### <a name="issue-resolution-2"></a>Řešení problému 2

Pokud váš pracovní postup používá přizpůsobený kód, po upgradu systému mohou nastat problémy. Například ve workflowu deníku může být tlačítko **Odeslat** šedé, takže jej nemůžete vybrat, chcete-li schválit odeslání.

Pokud je tlačítko **Odeslat** šedé, váš pracovní postup mohl být přizpůsoben, což znamená, že metoda workflowu `canSubmitToWorkflow()` v `FormDataUtil` byla rozšířena. Chcete-li tento problém vyřešit, změňte způsob, jakým rozšiřujete metodu `canSubmitToWorkflow()` k použití struktury v následujícím příkladu.

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

### <a name="issue-resolution-3"></a>Řešení problému 3

Pokud se problém týká pouze několika konkrétních uživatelů, nemusí mít tito uživatelé oprávnění zabezpečení, která jsou vyžadována ke spuštění operací pracovního postupu v denících zásob. Ověřte, že každý ovlivněný uživatel má bezpečnostní oprávnění *Udržovat pracovní postup deníku zásob*. Ve výchozím nastavení je toto oprávnění přiřazeno k povinnosti, která má stejný název, a tato povinnost je aplikována na roli *Skladník* a *Manažer skladu*.

## <a name="my-inventory-journal-remains-in-system-locked-status-and-the-workflow-batch-job-doesnt-work"></a>Můj deník zásob zůstává ve stavu uzamčeného systému a dávková úloha pracovního postupu nefunguje.

### <a name="issue-description"></a>Popis problému

Jeden z vašich deníků zásob je uzamčen nějakou operací a není uvolněn. Například pokud během zaúčtování dojde k neznámé chybě (což je operace uzamčení systému), deník může zůstat ve stavu uzamčeného systému. V tomto případě obslužná rutina pracovní položky pracovního postupu vyvolá chybu, zatímco provede ověření zámku.

### <a name="issue-resolution"></a>Řešení problému

Přihlaste se k instanci serveru SQL Server pro Supply Chain Management a zkontrolujte, zda je **InventJournalTable.SystemBlocked** nastaven na *1*. Pokud ano, ujistěte se, že deník by neměl být v uzamčeném stavu, a poté resetujte **InventJournalTable.SystemBlocked** na *0*.

## <a name="my-inventory-journal-workflow-is-never-completed-and-the-journal-cant-be-edited-or-posted"></a>Můj pracovní postup deníku zásob není nikdy dokončen a deník nelze upravit ani zaúčtovat.

### <a name="issue-description"></a>Popis problému

Po odeslání pracovního postupu schválení deníku přestane zpracování pracovního toku reagovat a vy nebudete moci upravovat ani zpracovávat deníky.

### <a name="issue-resolution"></a>Řešení problému

Existuje několik důvodů, proč zpracování workflowu nemusí být provedeno. Zkontrolujte následující problémy:

- Jděte na **Řízení zásob &gt; Nastavení &gt; Workflowy správy skladu** a zkontrolujte konfiguraci ovlivněného workflowu. Další informace naleznete v tématu [Workflowy schválení deníku](inventory-journal-workflow.md).
- Ve workflowu může docházet k výjimce nebo chybě. Zkontrolujte historii pracovní položky ovlivněného workflowu, abyste zjistili, zda obsahuje chybu aplikace, která workflow ukončí.
- Deník zásob lze aktualizovat nebo upravovat, pouze pokud je schválen. Pokud je vyvolání aktivní, můžete se pokusit vyvolat deník. Provádění dávkové úlohy workflowu může být pozastaveno z několika důvodů. Některé z těchto důvodů mohou být způsobeny problémem rámce workflowu.

## <a name="inventory-journal-workflow-conditions-apply-only-at-the-journal-level-not-at-the-line-level"></a>Podmínky workflowu deníku zásob platí pouze na úrovni deníku, nikoli na úrovni řádků

### <a name="issue-description"></a>Popis problému

K tomuto problému může dojít, pokud se například pokusíte nastavit podmínku workflowu deníku zásob na částku nákladů. Nastavíte podmínku tak, aby byl krok 1 spuštěn pouze v případě, že částka nákladů bude nižší než 100. Pak nastavíte jinou podmínku tak, aby byl krok 2 spuštěn pouze v případě, že částka nákladů bude vyšší nebo rovna 100. Poté, když je spuštěn workflow, se v historii pracovního postupu zobrazuje pouze jeden řádek a první podmínka se vždy vyhodnotí jako *skutečný*, bez ohledu na hodnotu, která je zadána.

### <a name="issue-workaround"></a>Řešení problému

V aktuální verzi platí podmínky workflowu deníku zásob pouze na úrovni deníku, nikoli na úrovni řádků. Toto chování je záměrné. Doporučujeme nastavit kritéria podmínky pouze na atributy na úrovni deníku.

## <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-filter-results-as-i-expect"></a>Podokno filtru na stránce množství po ruce nefiltruje výsledky podle mého očekávání.

### <a name="issue-description"></a>Popis problému

Filtry v podokně filtru na stránce **seznam na skladě**  nefiltrují výsledky podle mého očekávání.

### <a name="issue-resolution"></a>Řešení problému

Toto chování je záměrné.

Stránka  **Seznam na skladě**  je sestavena z podrobné tabulky zásob na skladě, která obsahuje všechny dostupné rozměry. Seznam na této stránce je však shrnutím. Proto by mohl kombinovat řádky ze zdrojové tabulky agregováním hodnot podle zobrazených rozměrů.

Filtry, které jsou nastaveny v podokně filtrů se vztahují na zdrojovou tabulku, nikoli na agregovaný seznam. Toto chování může někdy způsobit neočekávané výsledky, jak je uvedeno v [těchto příkladech](inventory-on-hand-list.md#examples).

Nicméně  [filtry poskytované v mřížce](inventory-on-hand-list.md#grid-filters) *platí*  pro agregovaný seznam. Tyto filtry zahrnují QuickFilter v horní části mřížky a filtr pro každou hlavičku sloupce.

## <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a>Jednotka a množství jednotky nepracují správně v deníku zásob.

### <a name="issue-description"></a>Popis problému

Při práci s jednotkami a množstvími v deníku zásob se můžete setkat s jedním nebo oběma z následujících problémů:

- Když je pro vydaný produkt nastavena jednotka převodu, nevidíte v deníku zásob jednotky ani množství jednotek a nemůžete jednotku v deníku zásob změnit.
- V deníku zásob vidíte pole **Množství** a **Jednotka**, ale nevidíte pole **množství jednotky**. Pokud změníte jednotku, zadejte množství a zaúčtujete deník, deník stále zobrazuje původní měrnou jednotku pro toto množství.

### <a name="issue-resolution"></a>Řešení problému

Chcete-li opravit problém, postupujte následovně.

1. V pracovním prostoru **Správa funkcí** se ujistěte, že je zapnutá funkce *Použití měrné jednotky a jednotkového množství v denících zásob*. Tato funkce přidává pole **Jednotka** a **Jednotkové množství** do deníku.
1. Po zapnutí funkce použijte pole **Množství**, **Jednotkové množství**, a **Jednotka** následujícím způsobem:

    - **Množství** - Určete množství pomocí výchozí jednotky definované pro vydaný produkt. Samotná výchozí jednotka se zde však nezobrazuje. Pokud je nastaven převod mezi výchozí jednotkou a jednotkou vybranou v poli **Jednotka**, pole **Množství** se automaticky aktualizuje na základě výběrů v poli **Jednotkové množství** a v poli **Jednotka**.
    - **Jednotkové množství** – určete množství pro měrnou jednotku vybranou v poli **Jednotka**.
    - **Jednotka** - Vyberte jednotku, která se má použít pro hodnotu v poli **Jednotkové množství**.

## <a name="i-receive-the-following-error-message-maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a>Zobrazuje se následující chybová zpráva: „Maximální počet desetinných míst pro skladovou jednotku je 0.“

### <a name="issue-description"></a>Popis problému

Při pokusu o zaúčtování transakce zásob nebo rezervace zásob se zobrazí následující chybová zpráva: "Maximální počet desetinných míst pro jednotku udržování zásob je 0."

K tomuto problému dochází, když je množství transakce zásob zadáno jako desetinná hodnota, která je pod úrovní přesnosti, kterou pole podporuje. Například množství *0,5* bylo zadán pro transakci inventáře, ale jsou podporována pouze celočíselná množství. Hodnota by proto měla být *1* namísto *0,5*.

### <a name="issue-resolution"></a>Řešení problému

1. Spusťte následující skript na instanci serveru SQL Server a zaokrouhlete množství v transakcích zásob. Tento skript opraví hodnoty v tabulce **inventTrans**.

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. Spusťte kontrolu konzistence na skladě, kde je možnost **opravit chybu** zapnutá. Tato kontrola opraví hodnoty v tabulce **inventSum**.

> [!IMPORTANT]
> Důrazně doporučujeme, abyste skript pečlivě upravili podle potřeby pro své prostředí, otestovali jej v testovacím prostředí a poté zkontrolovali výsledná data před spuštěním skriptu v provozním prostředí.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]