--- 
title: "Zadání a porovnání nabídek pro požadavek na nabídku a přidělení smlouvy"
description: "Tento postup popisuje, jak zadat odpovědi na požadavek na nabídku, hodnocení a porovnání nabídek, a poté přijmout nabídku některého z dodavatelů."
author: mkirknel
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5dea9d7bfb1bf7b11f6c49cccaab1b73d4e58d16
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a>Zadání a porovnání nabídek pro požadavek na nabídku a přidělení smlouvy

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje, jak zadat odpovědi na požadavek na nabídku, hodnocení a porovnání nabídek, a poté přijmout nabídku některého z dodavatelů. Tento postup můžete projít v ukázkových datech společnosti USMF. Než začnete, musíte mít požadavek na nabídku se dvěma řádky, které byly odeslány nejméně dvěma dodavatelům. Pro vytvoření je nezbytným předpokladem vytvoření postupu "Vytvořit požadavek na nabídku". Je nutné nastavit kritéria hodnocení před spuštěním tohoto procesu.


## <a name="enter-a-reply-from-a-vendor"></a>Zadání odpovědi od dodavatele
1. Přejděte na Zásobování a zdroje > Požadavky na nabídky > Všechny požadavky na nabídky.
2. Vyberte požadavek na nabídku, který má stav Odesláno, a klepněte na odkaz u čísla případu s požadavkem na nabídku.
    * Požadavek na nabídku byl odeslán nejméně 2 dodavatelům.  
3. Klepnutím na záhlaví přejděte na seznam dodavatelů.
4. Vyberte dodavatele, pro kterého chcete zadat odpověď na požadavek na nabídku.
5. Klikněte na Zadat odpověď.
6. V podokně akcí klikněte na možnost Odpovědět.
7. Klikněte na Kopírovat data do odpovědi.
    * Touto akcí zkopírujete vybraná data, jako například množství z případu požadavku na nabídku do odpovědi na požadavek na nabídku. Také můžete tuto akci vynechat a vyplnit všechna pole s odpovědí ručně při úpravách odpovědi.  
8. Klikněte na položku Upravit.
9. Zadejte číslo do pole Jednotková cena.
10. Vyberte jiný řádek nabídky.
11. Zadejte číslo do pole Jednotková cena.

## <a name="score-the-bid"></a>Hodnocení nabídky
1. Klepnutím na záhlaví přejděte na hodnocení nabídek.
2. Rozbalte oddíl Hodnocení nabídky.
3. V poli Hodnocení zadejte číslo jednoho z kritérií hodnocení.
    * Pokud umístíte kurzor myši na některé z kritérií hodnocení, zobrazí se popisek pole s rozsahem požadovaných bodů. V této ukázce můžete přidat číslo do libovolného kritéria v rozmezí 1 až 5.  
4. Vyberte jiné kritérium hodnocení.
5. V poli Hodnocení zadejte číslo.
6. Rozbalte oddíl Dotazníky.
    * Má-li případ požadavku na nabídku dotazník, který byl odeslán dodavatelům, můžete zadat jejich odpovědi v části dotazníku.  
7. Zavřete stránku.

## <a name="enter-a-reply-for-another-vendor"></a>Zadání odpovědi pro jiného dodavatele
1. Vyberte dalšího dodavatele vymazáním dodavatele, pro kterého jste právě zadali odpověď a vyberte řádek u dalšího dodavatele.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Klikněte na Zadat odpověď.
4. Klikněte na Kopírovat data do odpovědi.
5. Klikněte na položku Upravit.
6. Zadejte číslo do pole Jednotková cena.
7. Vyberte jiný řádek nabídky.
8. Zadejte číslo do pole Jednotková cena.

## <a name="score-the-second-bid"></a>Hodnocení druhé nabídky
1. Klepnutím na záhlaví přejděte na hodnocení nabídek.
2. V poli Hodnocení zadejte číslo.
3. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
4. V poli Hodnocení zadejte číslo.

## <a name="compare-the-replies"></a>Porovnání odpovědí
1. V podokně akcí klikněte na položku Obecné.
2. Klikněte na Porovnat odpovědi.
3. Do pole Rozsah zadejte požadované číslo.
    * Na této stránce se zobrazí nabídky se záhlavím a řádky a celkovým hodnocením na úrovni záhlaví. Porovnat řádky můžete seřazením v mřížce tak, aby byly porovnatelné řádky vedle sebe. Informace zahrnují také následující:  Množství: množství nabízené dodavatelem. Toto množství se nemusí rovnat množství zadanému v RFQ.   Čistá částka: cena nabízená dodavatelem po odečtení všech slev za položky na řádku.   Odchylka: počet dnů, o které se datum dodání v záhlaví nabídky nebo řádku liší od požadovaného data dodání v záhlaví RFQ nebo řádku RFQ.   Pro každou nabídku můžete zadat hodnocení.  
4. Vyberte řádek záhlaví pro jinou objednávku, kterou chcete ohodnotit.
5. Do pole Rozsah zadejte požadované číslo.
6. Klikněte na položku Uložit.

## <a name="reject-a-bid"></a>Odmítnutí nabídky
1. Vyberte řádek záhlaví pro objednávku, kterou chcete odmítnout.
    * V každém okamžiku můžete je možné pouze přijetí, odmítnutí nebo návrat jedné nabídky nebo řádků v rámci nabídky.  
2. Vyberte Zaškrtnout políčko.
    * Pokud označíte pole Označit v záhlaví nabídky, budou označeny také všechny řádky. Můžete se také rozhodnout označit dílčí sadu řádků v rámci nabídky a odmítnout je nebo je přijmout. Lze potvrdit nabídku jednoho dodavatele pro některé řádky v požadavku na nabídku a potom udělit jiné řádky požadavku na nabídku jinému dodavateli. Musíte tak ale učinit ve 2 krocích vždy po jedné nabídce. Pokud existují řádky alternativy, můžete pouze přijmout buď původní řádek nabídky nebo jeho alternativu, ne však obojí.  
3. Klikněte na tlačítko Zamítnout.
4. Klepnutím na možnost Parametry otevřete dialogové okno.
5. V poli Odmítnutí důvodu zadejte nebo vyberte hodnotu.
    * Důvod pro odmítnutí bude uložen v odpovědi.  
6. Klikněte na tlačítko OK.
7. Klikněte na tlačítko OK.
8. Zavřete stránku.
9. Zavřete stránku.
10. Aktualizujte stránku.

## <a name="accept-a-bid"></a>Přijetí nabídky
1. Vyberte nabídku, kterou chcete přijmout, a klepněte na odkaz v poli Požadavek na nabídku.
2. V podokně akcí klikněte na možnost Odpovědět.
3. Klepněte na možnost Akceptovat.
    * Pokud jste označili určité řádky a jiné nikoli, akce přijetí bude obsahovat pouze označené řádky. Pokud chcete přijmout všechny řádky v nabídce, řádky není třeba označit.  
4. Klepnutím na možnost Parametry otevřete dialogové okno.
    * Tímto způsobem lze zaznamenat důvod pro přijetí nabídky. Důvod bude uložen v nabídce.  
5. V poli Potvrzení důvodu zadejte nebo vyberte hodnotu.
6. Klikněte na tlačítko OK.
7. Klikněte na tlačítko OK.
    * Po klepnutí na tlačítko OK vytvoříte nákupní objednávku na základě řádků, které jsou zahrnuty v přijetí požadavku na nabídku. Pokud existují jiné nabídky, které nebyly zpracovány (přijaty, odmítnuty nebo vráceny), systém zobrazí výzvu k odmítnutí zbývajících nabídek.  

## <a name="view-the-purchase-order-thats-been-generated"></a>Zobrazení nákupní objednávky, která byla vytvořena
1. V podokně akcí klikněte na položku Obecné.
2. Klikněte na Nákupní objednávku.
    * Zde je vidět nákupní objednávka, která byla vygenerována po přijetí nabídky.  
3. Zavřete stránku.
4. Zavřete stránku.
5. Zavřete stránku.
6. Zavřete stránku.


