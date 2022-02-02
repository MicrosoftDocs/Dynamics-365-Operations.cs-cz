---
title: Přidání nebo kopírování leasingů (Preview)
description: Toto téma popisuje, jak vytvořit nový leasing zadáním informací o něm do leasingu majetku nebo zkopírováním informací z existujícího leasingu.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b09a87c7d4f5ba076647218c3586d17a13e6c558
ms.sourcegitcommit: 7adf9ad53b4e6d1c4d5d612ce0977b76c61ec173
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/13/2022
ms.locfileid: "7967919"
---
# <a name="add-or-copy-leases-preview"></a>Přidání nebo kopírování leasingů (Preview)

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak vytvořit leasing od začátku v leasingu majetku, a také jak vytvořit leasing kopírováním existujícího leasingu. Proces vytváření leasingu od začátku zahrnuje zadání informací o novém leasingu a následné vytvoření plánu leasingu. Po vytvoření alespoň jednoho leasingu může být jednodušší zkopírovat informace ze stávajícího leasingu a poté tyto informace upravit podle potřeby k vytvoření nového leasingu.

## <a name="create-a-lease"></a>Vytvoření leasingu

Pomocí těchto kroků vytvoříte leasing v leasingu majetku.

1. Na stránce **Shrnutí leasingu** v podokně Akce vyberte **Nový**.
2. Zadejte informace o leasingu. Pole, která jsou povinná, mají červené ohraničení.

Počáteční datum leasingové splátky nemůže být dřívější než datum zahájení leasingu. Pokud zadáte počáteční datum leasingové platby, které je dřívější než počáteční datum leasingu, zobrazí se chybová zpráva.

Ve výchozím nastavení je možnost **Částka splátky** možnost na pevné záložce **Obecné** stránky **Údaje o leasingu** stránka je nastavena na **Ne**, pokud je možnost **Povolit splátky** na stránce **Parametry leasingu majetku** nastavena na **Ano**. 

Pokud je možnost **Částka splátky** nastavena na **Ano**, pole **Částka platby** na pevné záložce **Řádky splátkového kalendáře** je uzamčena. Bude nastavena na součet částek plateb, které jsou zadány později v katalogu **Rozpis částky platby**.

Vyberte **Rozpis splátek** k otevření stránky, kde můžete přidat jednotlivé typy plateb. Tlačítko **Přidat součty k částce platby** přesune součty na pole **Částka platby**.

> [!NOTE]
> Pokud přidáte položkovou částku platby a poté vyberete klávesu **Esc**, zadané částky nebudou přidány do pole **Částka platby** pole na pevné záložce **Řádky splátkového kalendáře**. Místo toho budou uloženy v dialogovém okně **Rozpis částky platby**. Pokud chcete, aby dialogové okno zobrazovalo celkovou částku, vyberte sloupec **Množství**, vyberte a podržte (nebo klikněte pravým tlačítkem) a poté vyberte **Celkem tento sloupec**. 

Tlačítko **Kopírovat řádek** zkopíruje podrobný rozpis plateb.

## <a name="create-a-lease-schedule"></a>Vytvoření plánu leasingu

Po dokončení zadávání informací o leasingu postupujte podle těchto kroků a vytvořte plán leasingu.

> [!NOTE]
> Finanční dimenze se mohou změnit na základě libovolných akýchkoli vlastních finančních dimenzí.

1. Volbou **Vytvořit plány** vygenerujete leasingové knihy. Leasingové knihy zahrnují splátkové, amortizační, odpisové a výdajové plány.
2. Chcete-li otevřít leasingové knihy a zobrazit nově vytvořené plány, vyberte kartu **Knihy**.

    Stránka **Podrobnosti o knize** ukazuje, jak je leasing zaúčtován v knihách, které k němu byly přiděleny. Odtud můžete zobrazit plány leasingu.

    Harmonogram plateb obsahuje vstupy z karty **Řádky platebního kalendáře** na stránce **Přidání leasingu**. Stále můžete změnit každou částku platby a variabilní platbu. Leasingový závazek se počítá na základě upraveného platebního kalendáře.

    > [!NOTE]
    > Počáteční datum leasingové splátky musí být stejné nebo pozdější než datum zahájení leasingu. Pokud zadáte počáteční datum platby, které je dřívější než počáteční datum leasingu, zobrazí se chybová zpráva. 

4. Po dokončení kontroly platebního kalendáře vyberte **Potvrdit kalendář**. Po potvrzení kalendáře již není leasing k dispozici pro úpravy.

    > [!NOTE]
    > Systém automaticky vypočítá dobu trvání leasingu z řádků platebního kalendáře na stránce **Přidání leasingu**.
    >
    > Aby systém vypočítal dobu trvání leasingu v měsících, vyhledá rozdíl mezi počátečním a konečným datem pro konkrétní řádek platebního kalendáře. Poté se přesune na další řádek platebního kalendáře a znovu vyhledá rozdíl. Nakonec systém sečte všechny částky k určení doby trvání leasingu v měsících.

5. Chcete-li zobrazit vypočítané období úrokových výdajů, otevřete stránku **Plán amortizace závazku**. Chcete-li zobrazit vypočítané lineární odpisy, otevřete stránku **Plán odpisu majetku**.
6. Poté, co dokončíte kontrolu vypočítané částky, můžete vytvořit položku deníku počátečního uznání na stránce **Počáteční uznání**. Zobrazí se zpráva, že deník byl vytvořen.

    > [!NOTE]
    > Položka deníku se nezaúčtuje do hlavní knihy, dokud ji ručně nezaúčtujete.

7. Chcete-li zkontrolovat navrhovanou položku počátečního uznání před jejím odesláním, vyberte **Deník leasingu majetku**.

    > [!NOTE]
    > Deník leasingu majetku nelze vytvořit ručně. Automaticky se vytvoří, když se vytvoří plány leasingu.

8. Až dokončíte kontrolu položky deníku počátečního uznání a jste připraveni ji zaúčtovat, volbou **Zaúčtovat** uznáte používaný majetek a leasingový závazek v hlavní knize.

## <a name="copy-a-lease"></a>Kopírování leasingu

Pronájem majetku vám umožňuje zkopírovat podrobnosti leasingu a vytvořit nový leasing, který má stejné informace. Poté můžete změnit pole leasingu, než vytvoříte plány kopírovaného leasingu.

1. Na stránce **Shrnutí leasingu** vyberte leasing, který chcete kopírovat, a poté v podokně akcí vyberte **Kopírovat leasing**.

    > [!NOTE]
    > Pokud je vypnutý parametr **Ručně** pro číselnou sekvenci ID leasingu, další číslo v sekvenci je automaticky generováno jako ID leasingu zkopírovaného leasingu. Pokud je zapnutý parametr **Ručně**, zobrazí se zpráva s výzvou k zadání ID leasingu, než budete pokračovat v kopírování leasingu.

2. Vyberte **Kopírovat**. Podrobnosti leasingu z vybraného leasingu jsou zkopírovány do nového leasingu. Poté můžete upravit podrobnosti nového leasingu, než jej uložíte, a vytvořit plány leasingu.

## <a name="asset-leasing-journal"></a>Deník leasingu majetku

Všechny položky deníku, které jsou vytvořeny v leasingu majetku, jsou obsaženy v deníku leasingu majetku. Na stránce **Deník leasingu majetku** (**Leasing majetku \> Položky deníku \> Deník leasingu majetku**), můžete filtrovat podle stavu zaúčtování, zobrazit konkrétní položky deníku a doklady a zaúčtovat nezaúčtované položky deníku.

> [!NOTE]
> Deník leasingu majetku nelze vytvořit ručně. Automaticky se vytvoří, když se vytvoří plány leasingu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
