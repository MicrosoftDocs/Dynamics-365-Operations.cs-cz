---
title: Blokování úvěru pro prodejní objednávky
description: V tomto tématu je popsáno nastavení pravidel používaných k blokování úvěru pro prodejní objednávky.
author: mikefalkner
manager: AnnBe
ms.date: 01/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8a0e006be8a72f35d6c6009ca9d67d083b8fac89
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124247"
---
# <a name="credit-holds-for-sales-orders"></a>Blokování úvěru pro prodejní objednávky
[!include [banner](../includes/banner.md)]

V tomto tématu je popsáno nastavení pravidel používaných k blokování úvěru pro prodejní objednávky. Pravidla blokování správy úvěrů lze použít pro jednotlivé odběratele nebo pro skupinu odběratelů. Pravidla blokování definují odpovědi za následujících okolností:

1. Počet dnů po splatnosti
2. Stav účtů
3. Platební podmínky
4. Úvěrový limit vypršel
5. Částka po splatnosti
6. Částka prodejní objednávky
7. Použitá část dostupného úvěru

Kromě toho existují dva parametry, které řídí další scénáře, jež budou blokovat prodejní objednávku.

1. Změna platebních podmínek
2. Změna slev na vyrovnání

## <a name="set-up-blocking-rules-and-exclusion-rules"></a>Nastavení pravidel blokování a vyloučení

Když odběratel zahájí prodejní transakci, informace o prodejní objednávce budou přezkoumány pomocí souboru pravidel blokování, která řídí rozhodnutí o tom, zda má nebo nemá být odběrateli poskytnut úvěr a umožněno pokračování prodeje. Můžete také definovat vyloučení, která zruší pravidla blokování a povolí zpracování prodejní objednávky. Pravidla blokování a pravidla vyloučení lze nastavit na stránce **Správa úvěru > Nastavení > Nastavení správy úvěru > Pravidla blokování**.

### <a name="days-overdue"></a>Dny po splatnosti

Otevřete záložku **Dny po splatnosti**, pokud se pravidlo blokování vztahuje na odběratele s jednou nebo více fakturami, které jsou určitý počet dní po splatnosti.
1. Vyberte rozsah odběratele **Platné pro**, který se se vztahuje k tomuto pravidlu.
   - Vyberte možnost **Tabulka**, pokud se pravidlo uplatňuje u určitého odběratele.
   - Vyberte možnost **Skupina**, pokud se toto pravidlo uplatňuje na úrovni skupiny odběratelů. 
   - Vyberte možnost **Vše**, pokud se pravidlo uplatňuje u všech odběratelů.
2. Jakmile určíte rozsah, musíte určit **Účet/skupinu**, které se budou v tomto rozsahu používat.
   - V případě rozsahu **Tabulka** vyhledávání nabídne seznam odběratelů, které lze vybrat. 
   - Vyberte možnost **Skupina**, pokud se pravidlo vztahuje na skupinu odběratelů podle limitu úvěru.
   - Vyberte možnost **Vše**, pokud se pravidlo uplatňuje u všech odběratelů. 
3. Vyberte možnost **Skupina podle rizika**, chcete-li použít kritéria pro uplatnění blokování úvěru u odběratelů, kteří jsou spojeni do skupiny na základě společného souboru faktorů, jako je například jejich hodnocení podle organizace Dun and Bradstreet, počet let podnikání, doba, po kterou jsou vašimi odběrateli, a tak dále.  
4. Vyberte typ pravidla, které nastavujete. Možnost **Blokování** vytvoří pravidlo, které zablokuje objednávku. Možnost **Vyloučení** vytvoří pravidlo, které vylučuje jiné pravidlo z blokování objednávky. 
5. Vyberte **Typ hodnoty**. Výchozí zadání je pevný počet dní. Pokud vytváříte vyloučení, můžete místo něj zadat pevný počet dní nebo částku. 
6. Zadejte počet dnů u hodnoty **Po splatnosti**, které budou povoleny pro vybrané pravidlo blokování, než bude objednávka blokována pro správu úvěru pro účely kontroly. Počet dnů po splatnosti představuje další počet dní odkladu, který je přičten k počtu dní od data splatnosti, po jejichž uplynutí je faktura považována za fakturu v prodlení. Pokud jste zadali **Typ hodnoty** jako částku pro vyloučení, zadejte částku a měnu pro tuto částku.

### <a name="accounts-status"></a>Stav účtů

Pokud pravidlo blokování platí pro odběratele s vybraným stavem účtu, otevřete záložku **Stav účtu**.
1. Vyberte typ pravidla, které nastavujete.  Možnost **Blokování** vytvoří pravidlo, které blokuje objednávku. **Vyloučení** vytvoří pravidlo, které bude vylučovat pravidlo z blokování objednávky. 
2. Vyberte možnost **Stav účtu**, která povede k zablokování prodejní objednávky pravidlem nebo jejímu vyloučení.

### <a name="terms-of-payment"></a>Platební podmínky

Vyberte možnost **Platební podmínky**, pokud se pravidlo blokování vztahuje na vybranou platební podmínku.
1. Vyberte typ pravidla, které nastavujete.  Možnost **Blokování** vytvoří pravidlo, které blokuje objednávku. **Vyloučení** vytvoří pravidlo, které bude vylučovat pravidlo z blokování objednávky. 
2. Vyberte možnost **Platební podmínky**, která povede k zablokování prodejní objednávky pravidlem nebo jejímu vyloučení.

### <a name="credit-limit-expired"></a>Úvěrový limit vypršel

Pokud se pravidlo blokování vztahuje na odběratele s limity úvěru, jejichž platnost vypršela, otevřete záložku **Vypršela platnost limitu úvěru**.
1. Vyberte rozsah odběratele **Platné pro**, který se se vztahuje k tomuto pravidlu.
   - Vyberte možnost **Tabulka**, pokud se pravidlo uplatňuje u určitého odběratele.
   - Vyberte možnost **Skupina**, pokud se toto pravidlo uplatňuje na úrovni Skupina odběratelů. 
   - Vyberte možnost **Vše**, pokud se pravidlo uplatňuje u všech odběratelů.
2. Jakmile určíte rozsah, musíte určit **Účet/skupinu**, která se v tomto rozsahu používá.
   - V případě rozsahu **Tabulka** vyhledávání nabídne seznam odběratelů, které lze vybrat. 
   - Vyberte možnost **Skupina**, pokud se pravidlo vztahuje na skupinu odběratelů v rámci správy úvěrů.
   - Vyberte možnost **Vše**, pokud se pravidlo uplatňuje u všech odběratelů. 
3. Chcete-li dále omezit seznam odběratelů, kteří budou blokováni ve správě úvěrů, vyberte možnost **Skupina podle rizika**. 
4. Vyberte typ pravidla, které nastavujete. 
   - Chcete-li vytvořit pravidlo, které blokuje objednávku, vyberte možnost **Blokování**. 
   - Chcete-li vytvořit pravidlo, které vyloučí jiné pravidlo z blokování objednávky, vyberte možnost **Vyloučení**. 
5. Zadejte hodnotu **Počet dnů od vypršení platnosti limitu úvěru** pro vybrané pravidlo blokování, které označují počet dnů, které uplynou, než bude objednávka blokována ve správě úvěrů. Počet dnů po splatnosti představuje další dny odkladu, které jsou přičteny k počtu dní od vypršení platnosti limitu úvěru.

### <a name="overdue-amount"></a>Částka po splatnosti

Pokud se pravidlo blokování vztahuje na odběratele s částkami po splatnosti, otevřete záložku **Částka po splatnosti**.
1. Vyberte rozsah odběratele **Platné pro**, který se se vztahuje k tomuto pravidlu.
   - Vyberte možnost **Tabulka**, pokud se pravidlo uplatňuje u určitého odběratele.
   - Vyberte možnost **Skupina**, pokud se toto pravidlo uplatňuje na úrovni Skupina odběratelů. 
   - Vyberte možnost **Vše**, pokud se pravidlo uplatňuje u všech odběratelů.
2. Jakmile určíte rozsah, musíte určit **Účet/skupinu**, která se v tomto rozsahu používá.
   - V případě rozsahu **Tabulka** vyhledávání nabídne možnost vyhledání odběratele. 
   - Vyberte možnost **Skupina**, pokud se pravidlo vztahuje na skupinu odběratelů v rámci správy úvěrů.
   - Vyberte možnost **Vše**, pokud se pravidlo uplatňuje u všech odběratelů. 
3. Chcete-li dále omezit seznam odběratelů, kteří budou blokováni ve správě úvěrů, vyberte možnost **Skupina podle rizika**. 
4. Vyberte typ pravidla, které nastavujete. 
   - Chcete-li vytvořit pravidlo, které blokuje objednávku, vyberte možnost **Blokování**. 
   - Chcete-li vytvořit pravidlo, které vyloučí jiné pravidlo z blokování objednávky, vyberte možnost **Vyloučení**. 
5. Zadejte hodnotu **Částka po splatnosti** pro vybrané pravidlo blokování, která označuje částku, při které bude objednávka blokována ve správě úvěrů za účelem kontroly. 
6. Vyberte možnost **Typ hodnoty** definující typ hodnoty, který bude použit také k testování míry využití limitu úvěru. Pravidla blokování vyžadují procentní hodnotu, ale pro vyloučení lze nastavit pevnou částku nebo procentní hodnotu. Prahová hodnota se vztahuje k limitu úvěru.
7. Zadejte hodnotu **Prahová hodnota limitu úvěru** pro vybrané pravidlo, která odpovídá hodnotě, při které bude odběratel blokován ve správě úvěrů. Může se jednat o částku nebo procentní hodnotu podle typu hodnoty, který je vybrán v poli Typ hodnoty.
8. Toto pravidlo kontroluje, zda je překročena **Částka po splatnosti** a **Prahová hodnota limitu úvěru**. 

### <a name="sales-order"></a>Prodejní objednávka 

Vyberte možnost **Prodejní objednávka**, pokud pravidlo blokování platí pro hodnotu prodejní objednávky.
1. Vyberte rozsah odběratele **Platné pro**, který se se vztahuje k tomuto pravidlu.
   - Vyberte možnost **Tabulka**, pokud se pravidlo uplatňuje u určitého odběratele.
   - Vyberte možnost **Skupina**, pokud se toto pravidlo uplatňuje na úrovni Skupina odběratelů. 
   - Vyberte možnost **Vše**, pokud se pravidlo uplatňuje u všech odběratelů.
2. Jakmile určíte rozsah, musíte určit **Účet/skupinu**, která se v tomto rozsahu používá.
   - V případě rozsahu **Tabulka** vyhledávání nabídne možnost vyhledání odběratele. 
   - Vyberte možnost **Skupina**, pokud se pravidlo vztahuje na skupinu odběratelů v rámci správy úvěrů.
   - Vyberte možnost **Vše**, pokud se pravidlo uplatňuje u všech odběratelů. 
3. Chcete-li dále omezit seznam odběratelů, kteří budou blokováni ve správě úvěrů, vyberte možnost **Skupina podle rizika**. 
4. Vyberte typ pravidla, které nastavujete.  
   - Chcete-li vytvořit pravidlo, které blokuje objednávku, vyberte možnost **Blokování**. 
   - Chcete-li vytvořit pravidlo, které vyloučí jiné pravidlo z blokování objednávky, vyberte možnost **Vyloučení**. 
5. Zadejte hodnotu **Částka prodejní objednávky** pro vybrané pravidlo blokování, která označuje částku, při které bude objednávka blokována ve správě úvěrů. 

Pravidlo prodejní objednávky zahrnuje další nastavení, které ruší všechna ostatní pravidla. Chcete-li vytvořit vyloučení, které uvolní prodejní objednávku bez použití jakýchkoli jiných pravidel, označte políčko **Uvolnit prodejní objednávku** na řádku vyloučení.

### <a name="credit-limit-used"></a>Použitý úvěrový limit

Vyberte možnost **Použitý limit úvěru**, pokud se pravidlo blokování vztahuje na použitou částku limitu úvěru odběratele.
1. Vyberte rozsah odběratele **Platné pro**, který se se vztahuje k tomuto pravidlu.
   - Vyberte možnost **Tabulka**, pokud se pravidlo uplatňuje u určitého odběratele.
   - Vyberte možnost **Skupina**, pokud se toto pravidlo uplatňuje na úrovni Skupina odběratelů. 
   - Vyberte možnost **Vše**, pokud se pravidlo uplatňuje u všech odběratelů.
2. Jakmile určíte rozsah, musíte určit **Účet/skupinu**, která se v tomto rozsahu používá.
   - V případě rozsahu **Tabulka** vyhledávání nabídne možnost vyhledání odběratele. 
   - Vyberte možnost **Skupina**, pokud se pravidlo vztahuje na skupinu odběratelů v rámci správy úvěrů.
   - Vyberte možnost **Vše**, pokud se pravidlo uplatňuje u všech odběratelů. 
3. Chcete-li dále omezit seznam odběratelů, kteří budou blokováni ve správě úvěrů, vyberte možnost **Skupina podle rizika**. 
4. Vyberte typ pravidla, které nastavujete.
   - Chcete-li vytvořit pravidlo, které blokuje objednávku, vyberte možnost **Blokování**. 
   - Chcete-li vytvořit pravidlo, které vyloučí jiné pravidlo z blokování objednávky, vyberte možnost **Vyloučení**. 
5. Vyberte hodnotu **Prahová hodnota zbytku**, která definuje procento limitu úvěru, které zablokuje prodejní objednávku. Pokud hodnota objednávky zvýší částku použitého limitu úvěru nad tuto procentní hodnotu, objednávka bude blokována. 

## <a name="put-a-sales-order-on-hold-based-on-other-criteria"></a>Zablokování prodejní objednávky na základě jiných kritérií
  
### <a name="rank-payment-terms"></a>Hodnotit platební termíny  

Můžete vynutit použití pravidel kontroly úvěru při změně platebních podmínek. Je nutné seřadit platební podmínky a přiřadit k nim hodnotu řazení. Pokud změníte platební podmínky objednávky na platební podmínky, které jsou řazeny výše než původní platební podmínky, bude objednávka odeslána správě úvěrů a bude vyžadovat schválení.

Pořadí platebních podmínek lze nastavit na stránce **Správa úvěru > Nastavení > Nastavení správy úvěru > Seřadit platební podmínky**.

1. Vyberte platební podmínky v poli **Platební podmínky** k seřazení; vyberete-li podmínku, zobrazí se její popis v poli **Popis**.
2. V poli **Pořadí** vyberte pořadí podmínky. Všechny tyto hodnoty jsou ve vzájemném vztahu, proto můžete použít hodnoty 1, 2, 3 nebo 10, 20, 30. Pro většinu platebních podmínek lze rovněž použít stejnou hodnotu, aby se kontrola úvěru spouštěla pouze jednou nebo dvěma platebními podmínkami.

### <a name="rank-settlement-discounts"></a>Hodnotit slevy při vypořádání   

Můžete vynutit použití pravidel kontroly úvěru při změně slev pro vyrovnání. Je nutné seřadit slevy pro vyrovnání a přiřadit k nim hodnotu řazení. Pokud změníte slevy pro vyrovnání na objednávce na jiné slevy pro vyrovnání, které jsou řazeny výše než původní slevy pro vyrovnání, bude objednávka odeslána správě úvěrů a bude vyžadovat schválení.

Pořadí platebních podmínek lze nastavit na stránce **Správa úvěru > Nastavení > Nastavení správy úvěru > Seřadit slevy pro vyrovnání**.

1. Vyberte **Platební slevu**, jejíž pořadí chcete nastavit. Zobrazí se **Popis** slevy pro vyrovnání.
2. Vyberte hodnotu **Pořadí**. Všechny tyto hodnoty jsou ve vzájemném vztahu, proto můžete použít hodnoty 1, 2, 3 nebo 10, 20, 30. Pro většinu slev pro vyrovnání lze rovněž použít stejnou hodnotu, aby se kontrola úvěru spouštěla pouze jednou nebo dvěma slevami pro vyrovnání.

## <a name="sequence-the-application-of-rules"></a>Posloupnost použití pravidel

Pravidla jsou spouštěna v určitém pořadí, které můžete změnit podle potřeb vaší organizace. 

- Jeden příklad pravidel vyloučení prodejní objednávky vám umožní zrušit všechna pravidla, která by mohla zablokovat prodejní objednávku. Vytvořte pravidlo vyloučení prodejní objednávky a označte možnost **Uvolnit prodejní objednávku**. Objednávka nebude blokována, pokud bude platit toto pravidlo vyloučení, a nebudou kontrolována žádná jiná pravidla.
- Pravidla blokování mohou blokovat objednávku.
- Pravidla vyloučení jsou spouštěna po pravidlech blokování. Pravidla vyloučení budou mít vliv pouze na pravidlo, u kterého jsou definována. 
- Pravidla blokování a vyloučení jsou spouštěna v pořadí Tabulka, Skupina, Vše. Vzhledem k tomuto pořadí zpracování je možné mít pravidlo blokování na úrovni Vše, které nebude spuštěno, protože je spuštěno pravidlo vyloučení na úrovni Tabulka nebo Skupina.
- Vyloučení neruší pravidlo blokování, pokud nejsou na stejné úrovni. Pravidlo vyloučení na úrovni skupiny například nezruší pravidlo blokování na úrovni skupiny. Nebudete muset nastavovat vyloučení na úrovni Vše, kromě výše uvedeného příkladu pravidla vyloučení prodejní objednávky. 

Chování pravidla **Použitý limit úvěru** se změní na základě nastavení pro parametr **Zkontrolovat limit úvěru pro prodejní objednávku**, který se nachází ve formuláři parametru Úvěr a inkasa.
- Je-li parametr nastaven na hodnotu Ne, pravidlo Použitý limit úvěru nebude spuštěno.
- Je-li parametr nastaven na hodnotu Ano a **Zpráva při překročení limitu úvěru** je nastavena na varování, zobrazí se při překročení limitu úvěru varování. Pravidla **Použitý limit úvěru** se spustí, abyste zjistili, zda máte pravidla, která chcete spustit. V tomto scénáři však obvykle nepřidáte žádná pravidla.
- Je-li parametr nastaven na hodnotu Ano a **Zpráva při překročení limitu úvěru** je nastavena na chybu, bude limit úvěru zkontrolován a objednávka bude blokována, pokud dojde k překročení limitu úvěru. Kromě toho budou pravidla **Použitý limit úvěru** spuštěna, abyste zjistili, zda existují další pravidla, která je třeba spustit. Nezobrazí se chybová zpráva, ale zobrazí se důvod blokování **Překročený limit úvěru**. 

## <a name="settings-that-will-change-the-way-an-order-is-placed-on-hold"></a>Nastavení, která změní způsob blokování objednávky.

Objednávky lze vyloučit ze správy úvěru i v případě, že jsou použita pravidla. 

- Pokud změníte nastavení **Vyloučit odběratele ze správy úvěru** na pevné záložce **Všichni odběratelé > Vybrat odběratele > Úvěr a inkasa** na **Ano**, nebudou zpracovávány žádné objednávky pro tohoto odběratele
- Pokud změníte hodnotu **Vyloučit ze správy úvěru** v **záhlaví prodejních objednávek** na pevné záložce **Správa úvěru** na **Ano**, pravidla správy úvěru nebudou zpracována. Toto nastavení může provést pouze úředník nebo správce úvěru.

## <a name="processing-orders-on-hold-using-the-credit-management-hold-list"></a>Zpracování blokovaných objednávek pomocí seznamu blokování správy úvěru

Seznam blokování pro správu úvěrů umožní správcům úvěrů zobrazit všechny prodejní objednávky, které byly blokovány, a umožní jim odstranit blokování, pokud byly problémy s úvěrem zmírněny. Na stránce **Seznam blokování pro správu úvěrů** se zobrazí všechny prodejní objednávky, které jsou blokovány. Seznam blokování lze zobrazit na stránce **Všechna blokování úvěru** (**Správa úvěru > Seznam blokování pro správu úvěru > Všechna blokování úvěru**).
Prodejní objednávky od všech právnických osob jsou odesílány do stejného seznamu blokování správy úvěru, což umožňuje centralizované zobrazení všech transakcí vyžadujících pozornost. Uživatelům se budou zobrazovat pouze informace týkající se právnických osob, ke kterým mají přístup.

Prodejní objednávku lze umístit na seznam blokování z následujících důvodů:
1. Odběratel má fakturu, která je po splatnosti po určený počet dnů. 
2. Objednávka má určitý stav účtu.
3. Objednávka má určité platební podmínky.
4. Odběratel má limit úvěru, jehož platnost vypršela.
5. Odběratel má částku po splatnosti a použil zadanou procentní hodnotu svého limitu úvěru.
6. Prodejní objednávka překračuje určitou částku.
7. Odběratel překročil určitou procentní hodnotu svého limitu úvěru.
8. Platební podmínky se liší od výchozích platebních podmínek pro odběratele.
9. Slevy pro vyrovnání se liší od výchozí slevy pro vyrovnání pro odběratele.

Důvod blokování je zobrazen pro každou prodejní objednávku v seznamu blokování. Existuje-li pro blokování více důvodů, důvod se zobrazí jako **Více**. Pomocí nabídky **Důvody blokování** v podokně Akce můžete zobrazit všechny důvody, proč byla prodejní objednávka blokována. **Důvody blokování** můžete zobrazit také v okně s fakty.

### <a name="releasing-orders-from-the-hold-list-for-processing"></a>Uvolnění objednávek ze seznamu blokování ke zpracování

Pokud jste znovu prohledali důvody blokování a provedli jste jejich zmírnění, můžete prodejní objednávky uvolnit pro další zpracování.

1) Vyberte řádek v seznamu blokování. Je možné uvolnit více objednávek výběrem více řádků.
2) Vyberte **Důvod uvolnění** pro objednávku, která byla vybrána pro uvolnění.  
3) Zadejte **Datum kontroly** pro každou objednávku, která byla vybrána k uvolnění.  
4) Vyberte nabídku **Uvolnění** v podokně akcí pro uvolnění objednávky. Tato nabídka bude k dispozici až poté, co budou vybrány transakce. Uživatel má k dispozici dvě možnosti:
   - Vyberte možnost **Se zaúčtováním**, chcete-li odebrat blokování a zaúčtovat dokument pomocí stejného procesu zaúčtování, který byl použit při blokování. Pokud bylo například blokováno potvrzení prodejní objednávky, bude potvrzení prodejní objednávky po uvolnění dokončeno. Zobrazí se formulář zaúčtování prodejní objednávky, který uživateli umožní zaúčtovat potvrzení.
   - Zvolte možnost **Bez zaúčtování**, chcete-li odebrat blokování bez jakéhokoli dalšího zpracování. Prodejní objednávku lze ručně zaúčtovat.

### <a name="rejecting-orders-in-the-hold-list"></a>Zamítnutí objednávek v seznamu blokování
Pomocí nabídky **Odmítnout** v podokně akcí můžete prodejní objednávku odmítnout.
1. Vyberte řádek v seznamu blokování. Je možné uvolnit více objednávek výběrem více řádků.
2. Objednávka bude odebrána ze seznamu blokování a záhlaví prodejní objednávky bude aktualizováno, tak aby zobrazovalo, že objednávka byla odmítnuta.

### <a name="automatically-releasing-credit-management-holds"></a>Automatické uvolnění blokování správy úvěru
Prodejní objednávky jsou umístěny do seznamu blokování na základě pravidel blokování. Některé důvody blokování se však mohou v čase měnit, pokud prodejní objednávka zůstane v seznamu blokování po určitou dobu. Odběratel může například zaplatit svůj účet a uvolnit svůj limit úvěru. 

Pomocí nabídky **Vyhodnotit pro uvolnění** můžete zkontrolovat prodejní objednávky v seznamu blokování a automaticky je uvolnit, pokud byl důvod blokování zmírněn.
1.  Vyberte nabídku **Vyhodnotit pro uvolnění**
2.  Vyberte možnost **Zpracovat pravidla blokování**, chcete-li zkontrolovat všechny prodejní objednávky. Vyberte možnost **Zpracovat pravidla blokování pro vybrané řádky**, chcete-li zkontrolovat pouze řádky, které jste vybrali.
3. Zobrazí se posuvník, aby bylo možné vybrat jednoho odběratele. Ponechejte rozevírací seznam pro všechny odběratele prázdný. 
4. Klepnete-li na tlačítko OK, je proces spuštěn na pozadí a můžete pokračovat v práci na jiných úlohách. Pokud před klepnutím na tlačítko OK zvolíte dávkové zpracování, bude proces po klepnutí na tlačítko OK spuštěn v dávce. Zpracování blokovaných objednávek v seznamu může chvíli trvat, proto použijte volbu Obnovit pro aktualizaci stavu objednávek. 
5.  Pokud již důvod blokování objednávky není platný, bude důvod blokování považován za neplatný a při zobrazení důvodů blokování se již nebude u tohoto důvodu zobrazovat značka zaškrtnutí.
6.  Pokud jsou všechny důvody blokování vymazány, je do seznamu důvodů blokování přidán nový důvod **Připraveno k uvolnění**. Prodejní objednávka může být automaticky uvolněna.
7.  Je-li parametr **Automaticky uvolnit** na záložce **Úvěr a inkasa > Nastavení > Parametry úvěru a inkas > Úvěr > Automatické uvolnění** nastaven na možnost **Se zaúčtováním**, budete vyzváni k zaúčtování pomocí formuláře zaúčtování pro dokument, který byl blokován.
8.  Je-li parametr **Automaticky uvolnit** na záložce **Úvěr a inkasa > Nastavení > Parametry úvěru a inkas > Úvěr > Automatické uvolnění** nastaven na možnost **Bez zaúčtování**, musíte objednávku zaúčtovat ručně.

### <a name="credit-management-approval-workflow"></a>Workflow schválení správy úvěru

Lze rovněž vytvořit **Workflow správy úvěru** za účelem kontroly uvolnění blokování úvěrů. Jakmile nastavíte workflow na stránce **Správa úvěru > Nastavení > Workflow správy úvěru**, budou objednávky označené pro uvolnění nebo odmítnutí odeslány do workflow, kde musí být před uvolněním nebo odmítnutím nejprve schváleny. 

Pokud do workflow zahrnete úlohy pro uvolnění se zaúčtováním nebo uvolnění bez zaúčtování, schválení workflow rovněž uvolní prodejní objednávku. Pokud však v procesu uvolnění dojde k chybě z důvodu chybějících informací o nastavení nebo z jiných příčin, budete muset odvolat prodejní objednávku z workflow, opravit problém, který způsobil chybu, a poté objednávku znovu odeslat do workflow.

Pokud do workflow nezahrnete úlohy pro uvolnění se zaúčtováním nebo uvolnění bez zaúčtování, bude proces schvalování workflow umožňovat jednoduché ruční uvolnění prodejní objednávky po dokončení schválení.

### <a name="forced-credit-hold"></a>Vynucené blokování úvěru  
  
V některých případech je nutné, aby byly prodejní objednávky blokovány, přestože objednávka nesplňuje kritéria pravidel blokování. Správce úvěru může být například upozorněn na problém u odběratele nesouvisející s úvěrem a rozhodnout se neprodleně ručně blokovat objednávky, dokud nedojde k odstranění problému. Pokud k takové situaci dojde, můžete ručně vynutit blokování objednávky.

1. Otevřete prodejní objednávku, kterou chcete blokovat.  
2. Vyberte možnost **Vynutit blokování úvěru** na záložce **Správa úvěru** v podokně akcí **Správa úvěru**.
3. Vyberte **Důvod vynuceného blokování**.
4. Klepněte na tlačítko **OK**. Prodejní objednávka bude vrácena do seznamu blokování pro správu úvěrů.

Můžete také vynutit blokování více objednávek pomocí stránky **Správa úvěru > Pravidelné úlohy > Vynucení blokování úvěru**. Můžete například blokovat všechny prodejní objednávky konkrétního odběratele.
1. Vyberte **Důvod vynuceného blokování**. 
2. Klepněte na možnost **Záznamy k zahrnutí**, chcete-li vybrat prodejní objednávky, které mají být blokovány. 
3. Klepněte na tlačítko **OK** pro zpracování vybraných prodejních objednávek.

Prodejní objednávky, které byly nuceně blokovány, nelze zpracovat pomocí workflow.

#### <a name="releasing-orders-that-were-added-to-the-credit-management-hold-list-with-a-forced-credit-hold"></a>Uvolnění objednávek přidaných do seznamu blokování pro správu kreditů s vynuceným blokováním úvěru
Prodejní objednávky, které mají vynucený důvod blokování, nelze automaticky uvolnit. Pokud byla prodejní objednávka vynuceně blokována a použili jste proces, který prodejní objednávky automaticky uvolňuje, prodejní objednávka se zobrazí jako **Připravena k uvolnění** a zůstane v seznamu blokování. Chcete-li objednávku uvolnit, musíte použít nabídku **Uvolnění**.
 
## <a name="free-text-invoices-orders-and-project-invoice-support-in-credit-management"></a>Volné faktury, objednávky a podpora projektových faktur ve správě úvěru 
Správu úvěru lze aktuálně použít pouze pro prodejní objednávky. Volné faktury, místo prodejních objednávek a objednávky kontaktního střediska použijí dočasné limity úvěru a pojištění/záruk, které přidáte k úpravě limitu úvěru. Nebudou používat pravidla blokování a v případě potíží s limitem úvěru nebudou uloženy do seznamu blokování.

Neexistuje podpora pro projektové faktury ve správě úvěrů.
