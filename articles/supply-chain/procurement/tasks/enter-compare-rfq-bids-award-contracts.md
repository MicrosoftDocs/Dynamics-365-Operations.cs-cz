---
title: Zadání a porovnání nabídek pro požadavek na nabídku a přidělení smlouvy
description: Toto téma vysvětluje, jak zadat odpovědi na požadavek na nabídku, hodnotit a porovnávat nabídky, a poté udělit smlouvu jednomu z dodavatelů.
author: mkirknel
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchRFQCaseTable, PurchRFQReplyTable, PurchRFQCompare, PurchRFQEditLines, PurchRFQEditLinesParameters, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7fbbae2f097f812e1eefd8a095d72aa1c284c757
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207641"
---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a>Zadání a porovnání nabídek pro požadavek na nabídku a přidělení smlouvy

[!include [banner](../../includes/banner.md)]

Toto téma vysvětluje, jak zadat odpovědi na požadavek na nabídku, hodnotit a porovnávat nabídky, a poté udělit smlouvu jednomu z dodavatelů. Tento postup můžete projít v ukázkových datech společnosti **USMF**.

Než začnete s tímto postupem, musíte mít požadavek na nabídku se dvěma řádky, který byl odeslán nejméně dvěma dodavatelům. Chcete-li vytvořit tento požadavek na nabídku, dokončete postup [Vytvoření požadavku na nabídku](create-request-quotation.md). Je nutné nastavit kritéria hodnocení před dokončením tohoto procesu.

Nabídku můžete zadat buď jako dodavatel, nebo nákupčí. Další informace o naleznete v tématu [Nastavení a správa dodavatelské spolupráce](../set-up-maintain-vendor-collaboration.md).

## <a name="enter-a-reply-as-a-vendor"></a>Zadání odpovědi jako dodavatel

1. Na řídicím panelu vyberte **Nabídky dodavatele**.
2. V seznamu **Pozvánky k nové nabídce** vyhledejte požadavek na nabídku, který byl právě odeslán. Vyberte požadavek na nabídku, u nějž chcete zkontrolovat, co bylo požadováno.
3. Vyberte **Přílohy požadavku na nabídku** pro kontrolu všech přidaných příloh.
4. Chcete-li vytvořit upravitelná pole, vyberte **Nabídka**. Povšimněte si, že pole **Průběh nabídky** je nastaveno **Odběratel aktualizuje**.
5. V záhlaví a řádcích zadejte hodnoty z odpovědi na nabídku.
6. Pokud mají být do nabídky přidány nějaké přílohy, vyberte možnost **Přílohy nabídky**.
7. Chcete-li zobrazit, zda jsou vyžadovány nějaké dokumenty, vyberte záložku s náhledem **Položky průvodce nabídkou**.
8. Chcete-li zobrazit, zda byl požadavek na nabídku změněn, vyberte záložku s náhledem **Dodatky**.
9. Vyberte záložku s náhledem **Dotazník**. Všechny dotazníky, které jsou zde uvedeny, musí být zodpovězeny.
10. Chcete-li zobrazit rozšířené informace o řádku, vyberte záložku s náhledem **Podrobnosti řádku**.
11. Vyberte **Resetovat z požadavku na nabídku** pouze v případě, že je nutné obnovit hodnoty zadané do původních hodnot požadavku na nabídku.
12. Nabídku můžete kdykoli uložit a později provést další zpracování za předpokladu, že nevypršelo datum a čas platnosti. V takovém případě můžete najít nabídku v seznamu **Probíhající nabídky** v pracovním prostoru **Nabídky dodavatele**.
13. Jakmile je nabídka připravena k odeslání, vyberte možnost **Odeslat.** Vyberte **Odmítnout**, pokud se nechcete nabídky účastnit. Odeslané nabídky jsou k dispozici v seznamu **Odeslané nabídky** v pracovním prostoru **Nabídky dodavatele**.  
14. Po odeslání nabídky ji lze kdykoli znovu vyvolat před datem a časem vypršení platnosti. Všimněte si, že když je nabídka odvolána, není považována za odeslanou. Když je nabídka akceptována nebo zamítnuta oddělením zásobování, objeví se buď v seznamu **Přidělené nabídky** nebo **Ztracené nabídky** v pracovním prostoru **Nabídky dodavatele**.  

## <a name="enter-a-reply-from-a-vendor-as-a-procurement-professional"></a>Zadání odpovědi od dodavatele jako nákupčího

1. Zkontrolujte, zda je nastaveno oprávnění k úpravám nabídek dodavatelů. Přejděte na **Zásobování a zdroje \> Nastavení \> Parametry modulu Zásobování a zdroje**. Na kartě **Požadavky na nabídky** nastavte možnost **Nákupčí může upravit nabídku dodavatelů** na **Ano**.
2. Přejděte na **Zásobování a zdroje \> Požadavky na nabídky \> Všechny požadavky na nabídky**.
3. Vyberte požadavek na nabídku, který má stav **Odesláno**, a zvolte odkaz v poli **Případ požadavku na nabídku**.
4. Zvolte **Spravovat odpovědi**. Zobrazí se stránka požadavku na nabídku pro každého dodavatele, který byl pozván k nabídce.
5. Vyberte požadavek na nabídku, na který nebylo odpovězeno. (Pole **Průběh odpovědi** by mělo být nastaveno na **Nezahájeno**.)
6. Vyberte **Upravit \> Upravit odpověď na požadavek na nabídku**. Zobrazí se stránka **Odpověď na požadavek na nabídku**. Jako nákupčí můžete nyní zadat odpověď jménem dodavatele. Povšimněte si, že pole **Průběh nabídky** je nastaveno **Nákupčí aktualizuje**.  
7. Zadejte data nabídky. Po dokončení zvolte **Odeslat**.

## <a name="score-the-bids"></a>Hodnocení nabídek

1. Na stránce **Všechny požadavky na nabídky** vyberte případ požadavku na nabídku, pro který chcete vyhodnotit odpovědi.
2. Zvolte **Spravovat odpovědi**.
3. Vyberte odpověď na skóre.
4. Vyberte **Záhlaví**, aby bylo možné zobrazit hodnocení nabídky.
5. Na záložce s náhledem **Hodnocení nabídky** zadejte číslo do pole **Skóre** pro jedno z kritérií hodnocení. Pokud umístíte kurzor myši na jedno z kritérií hodnocení, zobrazí se popisek pole s požadovaným rozsahem skóre. V této ukázce můžete zadat číslo v rozmezí 1 až 5 pro libovolné kritérium hodnocení.  
6. Zopakujte krok 5 pro jiné kritérium hodnocení.
7. Má-li případ požadavku na nabídku dotazník, který byl odeslán dodavatelům, můžete zadat odpovědi dodavatele na záložce s náhledem **Dotazník**.
8. Zavřete stránku.
9. Zopakujte kroky 1 až 8 pro všechny ostatní nabídky.

## <a name="compare-the-replies"></a>Porovnání odpovědí

1. V podokně akcí na kartě **Obecné** zvolte **Porovnat odpovědi**.
2. Do pole **Rozsah** zadejte číslo.  
    - Na této stránce se zobrazí nabídky spolu s informacemi o záhlaví a řádku a také celkové skóre na úrovni záhlaví. Porovnat řádky můžete seřazením mřížky tak, aby byly porovnatelné řádky vedle sebe. Jsou obsaženy i následující informace:
    - **Množství** - Množství nabízené dodavatelem. Toto množství se nemusí rovnat množství zadanému v RFQ.
    - **Čistá částka** - Cena, kterou nabídl dodavatel za položky na řádku po odečtení všech slev.
    - **Odchylka** - Počet dnů, o které se datum dodání v záhlaví nabídky nebo řádku liší od požadovaného data dodání v záhlaví nebo řádku požadavku na nabídku. Pro každou nabídku můžete zadat hodnocení.  
3. Vyberte řádek záhlaví pro jinou objednávku, kterou chcete ohodnotit.
4. Do pole **Rozsah** zadejte číslo.
5. Zvolte **Uložit**.

## <a name="reject-a-bid"></a>Odmítnutí nabídky

1. Vyberte řádek záhlaví pro objednávku, kterou chcete odmítnout. V každém okamžiku je možné přijetí, odmítnutí nebo vrácení pouze jedné nabídky nebo řádků v rámci jedné nabídky.
2. Vyberte políčko **Označit**.  
    - Pokud označíte pole **Označit** v záhlaví nabídky, budou označeny také všechny řádky. Chcete-li odmítnout nebo přijmout pouze některé řádky nabídky, můžete označit pouze tyto řádky. Dále můžete přijmout nabídku jednoho dodavatele pro některé řádky požadavku na nabídku a poté přidělit jiné řádky požadavku na nabídku jinému dodavateli. Je však nutné dělat jednu nabídku současně.  
    - Pokud existují alternativní řádky, můžete přijmout buď původní řádek nabídky nebo jeho alternativu, nikoli však obojí.  
3. Vyberte **Odmítnout**.
4. Vyberte **Parametry** a pak v poli **Důvod odmítnutí** zadejte nebo vyberte důvod odmítnutí nabídky. Důvod je uložen v odpovědi.  
5. Vyberte **OK**.
6. Vyberte **OK**.

## <a name="accept-a-bid"></a>Přijetí nabídky

1. Vyberte nabídku, kterou chcete přijmout, a zvolte odkaz v poli **Požadavek na nabídku**. Pokud se nacházíte na stránce **Porovnat odpovědi na požadavky na nabídku**, je zvýrazněná nabídka tou nabídkou, kterou systém bude při akci přijetí brát v úvahu. Řádky lze přijímat pouze z jedné nabídky najednou.  
2. V podokně akcí zvolte **Odpovědět**.
3. Zvolte **Přijmout**. Pokud jste označili pouze určité řádky, bude akce přijetí zahrnovat pouze tyto řádky. Pokud chcete přijmout všechny řádky v nabídce, řádky nemusíte označit.  
4. Vyberte **Parametry** a pak v poli **Důvod přijetí** zadejte nebo vyberte důvod přijetí nabídky. Důvod je uložen v nabídce.  
5. Vyberte **OK**.
6. Vyberte **OK**. Po zvolení **OK** se vytvoří nákupní objednávka na základě řádků, které jsou zahrnuty v přijetí požadavku na nabídku. Pokud existují jiné nabídky, které nebyly zpracovány (přijaty, odmítnuty nebo vráceny), systém zobrazí výzvu k jejich odmítnutí.  

## <a name="view-the-purchase-order-that-is-generated"></a>Zobrazení generované nákupní objednávky

V podokně akcí na kartě **Obecné** zvolte **Nákupní objednávka**. Zobrazená stránka ukáže nákupní objednávku, která byla vygenerována po přijetí nabídky.
