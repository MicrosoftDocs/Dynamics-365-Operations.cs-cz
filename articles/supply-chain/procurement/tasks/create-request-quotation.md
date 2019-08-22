---
title: Vytvoření požadavku na nabídku
description: Tato procedura popisuje způsob ručního vytváření požadavku na nabídku.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchCreateRFQCase, InventLocationIdLookup, PurchRFQCaseTable, InventItemIdLookupSimple, EcoResCategorySingleLookup, UnitOfMeasureLookup, PurchRFQEditLines, PurchRFQEditLinesPrintOptions, VendRFQJournal, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3e35dbc489608c0aa3bfb13db5ae237f854612b1
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844105"
---
# <a name="create-a-request-for-quotation"></a>Vytvoření požadavku na nabídku

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tato procedura popisuje způsob ručního vytváření požadavku na nabídku. Toto by obvykle prováděl nákupčí. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat. Než začnete, je třeba nastavit typy oslovení. Po dokončení tohoto úkolu a po vytvoření a odeslání požadavku na nabídku můžete zadat odpovědí pro každého dodavatele, porovnat je a nejlepší smlouvu vybrat.


## <a name="prepare-a-new-rfq"></a>Příprava nového požadavku na nabídku
1. Přejděte na **Navigační podokno > Moduly > Zásobování a zdroje > Požadavky na nabídky > Všechny požadavky na nabídky**.
2. Klepněte na možnost **Nový**.
    K dispozici jsou následující typy nákupu – Nákupní objednávka (výchozí): dokument, který potvrzuje nabídku pro zakoupení produktů nebo přijetí nabídky pro prodej produktů za úplatu. Nákupní žádanka: tento typ je automaticky zaškrtnut, pokud vytvoříte RFQ přímo z nákupní žádanky. Při ručním výběru této možnosti se zobrazí chybové hlášení. Nákupní smlouva: dohoda o nákupu určitého množství nebo hodnoty produktu během času. Pokud vyberete tuto možnost, je nutné vybrat rozsah dat, který se vztahuje na nákupní smlouvu.  
3. Do pole **Název dokumentu** zadejte hodnotu.
4. V poli **Typ oslovení** zadejte nebo vyberte hodnotu.
    + Pokud je s typem oslovení spojena metoda hodnocení, tato funkce poslouží jako výchozí metoda hodnocení pro vytvářený požadavek na nabídku. Metodu hodnocení je možné změnit později.  
    + Zadejte datum do pole **Datum dodání**.  
    + Vyberte datum, k němuž chcete obdržet položky.  
    + Do pole **Datum a čas vypršení platnosti zadejte datum a čas**.  
    + Zadejte datum a čas, do kdy musí dodavatelé odpovědět na požadavek na nabídku.  
5. V poli **Sklad** zadejte nebo vyberte hodnotu. Jako výchozí dodací adresa je nastavena adresa skladu.  
6. Klikněte na tlačítko **OK**.

## <a name="add-lines"></a>Přidat řádky

Po zadání základních informací o RFQ je třeba zadat zboží nebo služby, pro které chcete vytvořit nabídku od dodavatelů. Položka je výchozí typ řádku.

1. V poli **Číslo položky** zadejte nebo vyberte hodnotu. Pokud používáte data USMF, můžete vybrat T0020.  
2. Zadejte číslo do pole **Množství**.
3. Klikněte na **Přidat řádek**.
4. V poli **Typ řádku** vyberte Kategorie. Můžete použít typ Řádek kategorie a vytvořit požadavky na nabídku pro položky bez skladu zboží nebo služeb. Poté musíte vybrat typ zboží nebo služeb z hierarchií kategorií zásobování.  
5. V poli **Kategorie zásobování** zadejte nebo vyberte hodnotu.
6. Do pole **Název produktu** zadejte hodnotu.
7. Zadejte číslo do pole **Množství**.
8. V poli **Jednotka** zadejte nebo vyberte hodnotu.

## <a name="add-vendors"></a>Přidat dodavatele
1. Klepnutím na **Záhlaví** můžete změnit zobrazení řádků na zobrazení záhlaví. 
2. Rozbalte sekci **Dodavatel**.
3. Klikněte na **Automatické přidání dodavatelů**. Můžete přidávat dodavatele do RFQ automaticky podle kategorie zásobování požadovaných položek. Pokud nejsou na řádcích zahrnuti žádní schválení dodavatelé pro kategorie, můžete je přidat ručně.  
4. Klikněte na tlačítko **Přidat**.
5. V poli **Účet dodavatele** zadejte nebo vyberte hodnotu.
6. Klikněte na tlačítko **Přidat**.
7. V poli **Účet dodavatele** zadejte nebo vyberte hodnotu. Jakmile vyberete dodavatele, změní se stav na Vytvořeno. To znamená, že informace o dodavateli jsou uloženy do RFQ, ale nebyly odesláno RFQ dodavateli. Dodavatele lze přidat do RFQ bez ohledu na stav dodavatele.  

## <a name="send-the-rfq-to-vendors"></a>Odešlete RFQ dodavatelům
1. V **podokně akcí** klikněte na možnost **Odeslat**. Na stránce Odesílání požadavku na nabídku se ujistěte, že dodavatelé v seznamu jsou dodavateli, kteří mají přijmout požadavek na nabídku.  
2. Klepněte na položku **Tisk**. Toto dialogové okno umožňuje vytisknout požadavek na nabídku. Pokud zvolíte tisk listu s odpovědí, obsah bude definován v parametrech zásobování a zdroje. Chcete-li vybrat, jak vytisknout list s odpovědí po otevření dialogového okna Tisk, klepněte na Rozšířené možnosti tisku. Bude vytištěn jeden požadavek na nabídku pro každého dodavatele, který obsahuje řádky se stavem Vytvořeno neb Odesláno. Zrušené řádky a řádky s registrovanými odpověďmi nebudou vytištěny.   
3. Klepněte na možnost **Zrušit**.
4. Klikněte na tlačítko **OK**.
5. Zavřete stránku.
6. Zavřete stránku.

## <a name="view-the-rfq-journal"></a>Zobrazení deníku požadavku na nabídku
1. Přejděte na **Zásobování a zdroje > Požadavky na nabídky > Požadavek na zpracování nabídek > Deníky požadavků na nabídku**.
2. Klikněte na **Náhled/tisk**.
3. Klepněte na **Náhled originálu**.
4. Zavřete stránku.
5. Zavřete stránku.

