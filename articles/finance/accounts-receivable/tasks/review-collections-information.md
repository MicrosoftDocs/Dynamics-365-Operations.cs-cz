---
title: Kontrola inkasních informací
description: Toto téma vysvětluje kontrolu informací inkasa společně s různými možnostmi nastavení a transakcemi inkasa.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustCollectionsPool, SysQueryForm, CustCollectionsAgent, OMTeamSelectMemberDialog, CustVendReportInterval, CustParameters, CustAgingSnapshot, CustVendAgingBucketLookUp, CustCollectionsPoolsListPage, CustCollectionsContactPart, CustCollections
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9bbfb6537118a9936c127018427b0516e7ea002a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971521"
---
# <a name="review-collections-information"></a>Kontrola inkasních informací

[!include [banner](../../includes/banner.md)]

Toto téma vysvětluje kontrolu informací inkasa společně s různými možnostmi nastavení a transakcemi inkasa. Tato procedura používá ukázkovou společnost USMF.

## <a name="create-customer-pools"></a>Vytvořte fondy odběratele
1. V navigačním podokně přejděte na **Moduly > Kredit a inkasa > Nastavení > Fondy zákazníků**.
- Použijte tuto stránku k nastavení fondů zákazníků, které představující dotazy, jež definují skupinu odběratelských účtů, které lze zobrazit a spravovat v rámci procesu inkasa nebo sledování splatnosti. Vyberte fondy zákazníků§ k filtrování informací pro stránku **Inkasa** a na stránkách se souvisejícím seznamem. Fondy zákazníků slouží také k filtrování účtů zákazníka, které budou zahrnuty při vytváření snímků pro sledování splatnosti.  
- Fondy zákazníků slouží k filtrování účty zákazníků, které budou zahrnuty při vytváření snímků pro sledování splatnosti.  
2. Zvolte **Nové**.
3. Do pole **ID fondu** zadejte hodnotu.
4. Do pole **Popis fondu** zadejte hodnotu.
5. Klikněte na možnost **Vybrat kritéria fondu**.
6. Zadejte hodnotu do pole **Kritéria**.
7. Vyberte **OK**.
8. Vyberte **Náhled fondu zákazníků**.

## <a name="create-collections-agents"></a>Vytvořte inkasní agenty
1. V navigačním podokně přejděte na **Moduly > Kredit a inkasa > Nastavení > Inkasní agenti**.  
- Na této stránce můžete nastavit zaměstnance jako inkasních agenty a volitelně jim přiřadit fondy zákazníků. *Inkasní agent* je osoba, která pracuje s odběrateli k zajištění, že platby se vybírají včas.  
- Inkasní agenti, kteří jsou nastaveni na této stránce, jsou automaticky přidáni do týmu inkasa. Pokud je vybrán tým v poli **Tým** na stránce **Parametry pohledávek účtu**, budou inkasní agenti přidáni do tohoto týmu. Pokud není vybrán tým, je automaticky vytvořen nový tým s názvem Inkasa a inkasní agenti jsou přidáni do tohoto týmu.  
2. Vyberte požadovaného agenta a poté na stránce vyberte **Přidat**.
3. V poli **ID fondu** vyberte požadovaný záznam v rozevírací nabídce.
4. Zaškrtněte políčko **Výchozí fond** nebo jeho zaškrtnutí zrušte.
- Vyberte tuto možnost, chcete-li pro vybraného inkasního agenta do seznamů filtru zahrnout všechny fondy zákazníků. Pokud tuto možnost nevyberete, budou k dispozici v seznamech filtru pouze ty fondy zákazníků, které jsou přiřazeny k inkasnímu agentovi.  

## <a name="create-aging-period-definition"></a>Vytvořit definici období pro sledování splatnosti
1. V navigačním podokně přejděte na **Moduly > Kredit a inkasa > Nastavení > Definice období pro sledování splatnosti**.
- Pomocí definic období pro sledování splatnosti lze analyzovat splatnost účtů dodavatelů a odběratelů v závislosti na zadaném datu. Každé období pro sledování splatnosti, kterému nastavíte definici období pro sledování splatnosti odpovídá sloupci na stránce seznamu, ve formuláři nebo v sestavě, po provedení analýzy.  
2. Zvolte **Nové**.
3. Zadejte hodnotu do pole **Období pro sledování splatnosti**.
4. Zadejte hodnotu do pole **Popis**.
- Zadejte název období, jednotku a interval pro každé období pro sledování splatnosti, které chcete zahrnout do definice období pro sledování splatnosti. Řádek, u něhož je v poli Jednotka uvedena hodnota 0 (nula), představuje datum spuštění analýzy. Řádky před tímto řádkem budou mít hodnotu -1 a řádky za tímto řádkem budou mít v poli Jednotka jako výchozí uvedenu hodnotu 1, ale lze je změnit. Změňte uspořádání řádků tlačítky **Nahoru** nebo **Dolů**. Řádek 0 (nula) nelze přesunout.  
- Nastavte ukazatel na místo, kam chcete vložit nový řádek, a poté vyberte **Přidat**.  
- Vyberte ukazatel představující období pro sledování splatnosti na formuláři **Inkasa** a stránce se seznamem. Například vyberte zelený indikátor pro aktuální období, žlutý indikátor pro 30 dnů minulého období a červený ukazatel pro 90 dnů minulého období.  
- Vyberte směr tisku pro definici období pro sledování splatnosti. Tento výběr určuje pořadí zobrazení sloupců v sestavě Sledování splatnosti odběratele nebo sestavě Sledování splatnosti dodavatele.  
  - Dopředu ؘ– Tisk sloupce ve stejném pořadí, ve kterém se záhlaví zobrazí v tabulce, počínaje prvním řádkem.  
  - Dozadu – Tisk sloupců v obráceném pořadí, než ve kterém se záhlaví zobrazí v tabulce, počínaje posledním řádkem.    

## <a name="setup-collections-parameters"></a>Nastavení parametrů inkasa
1. V navigačním podokně přejděte na **Moduly > Kredit a inkasa > Nastavení > Parametry pohledávek**.
2. Vyberte kartu **Inkasa**.
3. Rozbalte nebo sbalte oddíl **Výchozí hodnoty pro inkasování**.
- Vyberte definice období pro sledování splatnosti pro výchozí snímek sledování splatnosti, které bude použito ve formuláři **Inkasa**.  
- Vyberte tým, ke kterému jsou přiřazeni inkasní agenti ve formuláři **Inkasní agent**. Na seznamu se zobrazí pouze týmy, které mají typ Inkasa.  
4. Rozbalte nebo sbalte oddíl **Odpis**.
- Vyberte název deníku, který je nastaven pro denní deníky hlavní knihy, které se mají použit, když je transakce odepisována formulářem **Inkasa** souvisejících stránek seznamu.  
- Vyberte výchozí kód důvodu, který se použije při vytváření transakce odpisů pomocí formuláře **Inkasa** nebo souvisejících stránek se seznamem.  
- Vyberte tuto možnost, chcete-li vytvořit samostatný řádek deníku pro částky DPH při vytváření transakcí odpisů pomocí stránky **Inkasa** nebo souvisejících stránek se seznamem. Pokud vyberete tuto možnost, můžete snadno sledovat částky DPH, které se týkají transakcí odpisu. Částky DPH můžete sledovat samostatně, což umožňuje snadněji upravit povinnost k prodejní dani za ovlivněné období.  
5. Rozbalte nebo sbalte oddíl **Šablona e-mailu**.
- Vyberte šablonu e-mailů, která se má použít při odeslání e-mailové zprávy přes nabídku **E-mail > Transakce** pro akci kontaktu ve formuláři **Inkasa**.  
- Vyberte šablonu e-mailů, která se má použít při odeslání výpisu z účtu zákazníka jako přílohy e-mailové zprávy přes nabídku **E-mail > Výpis** akci kontaktu ve formuláři **Inkasa**.  
- Vyberte šablonu e-mailů, která se má použít při odeslání e-mailové zprávy přes nabídku **E-mail > Transakce** akci prodejce ve formuláři **Inkasa**.  

## <a name="age-customer-balance"></a>Splatný zůstatek odběratele
1. V navigačním podokně přejděte na **Moduly > Kredit a inkasa > Periodické úkoly > Splatné zůstatky odběratelů**.
- Vyberte definici období pro sledování splatnosti. Snímek sledování splatnosti udává splatnost transakcí na základě období pro sledování splatnosti určeného ve vybrané definici období pro sledování splatnosti.  
- Vyberte fond zákazníků nebo chcete-li vytvořit snímek sledování splatnosti pro všechny odběratele, ponechejte toto pole prázdné. Pokud je vybrána skupina odběratelů, proces snímku sledování splatnosti se použije pouze u účtů odběratelů, které jsou součástí fondu zákazníků. Vybraný fond zákazníků musí být typu Snímek sledování splatnosti.  
- Vyberte typ data, na kterém má být založen snímek sledování splatnosti.  
  - Datum transakce – Splatnost každé transakce bude založena na datu transakce.    
  - Datum splatnosti – Splatnost každé transakce bude založena na datu splatnosti.    
  - Datum dokumentu – Splatnost každé transakce bude založena na datu dokumentu.  
- Vyberte datum, které chcete použit jako aktuální datum pro snímek sledování splatnosti. Období pro sledování splatnosti se počítá na základě tohoto data.    
  - Aktuální datum – Použije se systémové datum. Tuto možnost použijte, pokud je zpracování nastaveno v opakujících se dávkách. Používáte-li toto datum, opakování dávky probíhá pravidelně a je použito systémové datum z daného okamžiku.    
  - Vybrané datum – Použije se vámi zadané datum. Pokud vyberete tuto možnost, zadejte datum pro sledování splatnosti.  
2. Vyberte **OK**.

## <a name="view-aged-customer-balances"></a>Zobrazit splatné zůstatky odběratelů
1. V navigačním podokně přejděte na **Moduly > Kredit a inkasa > Nastavení > Splatné zůstatky**.
- Tato stránka seznamu slouží k zobrazení zůstatků odběratelů a dlouhodobých částky podle období pro sledování splatnosti. Tyto informace jsou uloženy na snímku sledování splatnosti. Období pro sledování splatnosti je určeno podle použité definice období pro sledování splatnosti. Období pro sledování splatnosti je převzato z fondu zákazníků (pokud byl zadán v dotazu fondu). Pokud fond zákazníků nemá definici období pro sledování splatnosti, použije se výchozí definice období pro sledování splatnosti určené ve formuláři Parametry pohledávek.  
2. Rozbalte kartu **Kontakt**. Zde se zobrazí kontaktní informace:
- Kontaktní osoba pro inkaso pro odběratele.  
- Výchozí prodejce pro odběratele.  
3. Rozbalte kartu **Kreditní limit**.
- Použijte kartu **Informace o připsání** k zobrazení informací o kreditním limitu a aktuálním zůstatku pro odběratele.  

## <a name="view-customer-collections-details"></a>Zobrazit podrobnosti o upomínkách odběratele
1. Zkontrolujte, zda je vybrán požadovaný záznam.
2. Rozbalte okna s fakty **Adresa**, **Kontakt**, **Sledování splatnosti** a **Kreditní limit** a zobrazte příslušné informace.
3. V podokně akcí klikněte na možnost **Inkasovat**.
- Aktualizuje snímek sledování splatnosti pro zákazníka pomocí aktuálního data jako data sledování splatnosti, se kterým jsou porovnána data transakce. Pokud snímek sledování splatnosti obsahuje informace pro více právnických osob, aktualizovaný snímek sledování splatnosti obsahuje informace pro tuto sadu právnických osob. Částky jsou uloženy v zúčtovací měně právnické osoby, ke které jste přihlášeni při aktualizaci snímku pro sledování splatnosti.  
- Vyberte definici období pro sledování splatnosti. Ve výchozím nastavení je zobrazeno období pro sledování splatnosti přidružené ke snímku sledování splatnosti odběratele. Definice období pro sledování splatnosti určuje období pro sledování splatnosti a částky, které jsou zobrazeny v oknech s fakty **Splatné zůstatky** a **Informace o připsání** na stranu Dal.  
- Otevře nabídku obsahující následující položky:    
  - Společnost – Zobrazení částek okna s fakty Splatné zůstatky a Informace o připsání na stranu Dal ve zúčtovací měně právnické osoby.  
  - Odběratel – Zobrazení částek v okně s fakty Splatné zůstatky a Informace o připsání na stranu Dal v měně odběratele.  
- Vyberte jednu nebo více právnických osob ve snímek sledování splatnosti odběratele, pro kterého chcete zobrazit informace. Právnické osoby, které jsou zobrazeny na seznamu, byly vybrány když byl vytvořen snímek sledování splatnosti.  
- Zobrazení výkazu odběratele ve formátu aplikace Microsoft Excel. Můžete vybrat počáteční datum období transakce, které chcete zahrnout do výpisu a rozhodnout, zda mají být zahrnuty pouze otevřené transakce nebo otevřené a vyrovnané transakce. Pokud více právnických osob je zahrnuto ve snímku sledování splatnosti, transakce budou zahrnuty pro všechny právnické osoby.  
- Otevřete formulář **Dokumenty**, v němž můžete vytvořit nebo upravit dokumenty nebo poznámky.  
4. V podokně akcí vyberte možnost **Komunikovat**.  
- Otevřete aplikaci Outlook, kde můžete odeslat e-mailovou zprávu pro kontakt, který je určen v poli Kontakt. Pokud kontaktní osoba inkasa není zadána, je použita primární adresa zákazníka. Pokud není specifikován primární kontakt, e-mailové zprávy budou odeslány na první adresu uvedenou ve formuláři **Kontakty**. Vybrané transakce jsou zahrnuty jako příloha. Příloha je ve formátu aplikace Excel a obsahuje tří listy. Šablonu e-mailu pro zprávy kontaktům odběratele lze určit ve formuláři **Parametry pohledávek**.  
- Toto tlačítko není k dispozici, pokud kontakt vybraný v tomto formuláři nemá nastavenu e-mailovou adresu.  
- Připraví výkaz a otevře aplikaci Outlook, kde můžete odeslat e-mailovou zprávu s připojeným výpisem na adresu uvedenou v poli **Kontakt**. Pokud kontaktní osoba inkasa není zadána, je použita primární adresa zákazníka. Pokud není specifikován primární kontakt, e-mailové zprávy budou odeslány na první adresu uvedenou ve formuláři **Kontakty**.  
- Toto tlačítko není k dispozici, pokud kontakt vybraný v tomto formuláři nemá nastavenu e-mailovou adresu.  
- Otevře aplikaci Outlook, kde můžete odeslat e-mailovou zprávu zaměstnanci, který je zadán jako prodejní zástupce pro skupinu prodeje, která je přiřazena k odběrateli. Pokud jsou transakce vybrány, budou zahrnuty jako příloha. Příloha je ve formátu aplikace Excel a obsahuje dva listy. Šablonu e-mailu pro zprávy prodejce lze určit ve formuláři **Parametry pohledávek**.  
- Toto tlačítko není k dispozici, pokud prodejce zobrazený v tomto formuláři nemá nastavenu e-mailovou adresu.  
- Můžete si zobrazit transakce odběratele a provádět pro ně akce. Pokud používáte centralizované platby, budou zahrnuty informace pro všechny právnické osoby, které jsou součástí snímek sledování splatnosti odběratele. Informace o právnické osobě můžete omezit výběrem tlačítka **Společnost** ve skupině **Vybrat** v podokně akcí.  
- Změňte stav inkasování vybraných transakcí.    
  - Není sporné – U transakce nedošlo k inkasní akci.    
  - Sporné – Odběratel byl upozorněn, že došlo k potížím s transakcí.    
  - Přislíbeno zaplatit – Odběratel souhlasil s úhradou částky transakce.    
  - Vyřešeno – S transakcí byly vyřešeny všechny problémy a nejsou nutné žádné další inkasní akce.  
- Otevře nabídku a vyberte některou z následujících možností pro určení transakcí, které chcete zobrazit v tomto formuláři:    
  - Otevřít – zobrazí se pouze transakce, které nebyly vyrovnány.    
  - Otevřené a uzavřené – Zobrazit všechny transakce, vyrovnané i nevyrovnané.  
- Zpracování vybrané platby jako platby s nedostatečnými finančními prostředky (NFP).    
  - Toto tlačítko je k dispozici, pouze pokud vybraná transakce je platba (kreditní zůstatek bez faktury) zadaná do deníku plateb, k transakci je přiřazen bankovní účet a platba nebyla dříve zrušena.  
- Odepsat vybrané transakce.  
- Označte vybrané transakce pro vyrovnání mezi sebou.  
- Otevře formulář **Původní dokument**, ve kterém můžete zobrazit a vytisknout dokumenty pro vybranou transakci.  
- Otevře **nabídku** obsahující následující položky:    
  - Kolekce – zobrazeny budou pouze aktivity, které byly vytvořeny v inkasním formuláři.    
  - Vše – Zobrazení všech aktivit odběratele, bez ohledu na to, kde byly vytvořeny.  
- Otevře **nabídku** obsahující následující položky:    
  - Otevřít – zobrazeny budou pouze aktivity, které nebyly uzavřeny.    
  - Otevřené a uzavřené – Zobrazení všech aktivit, bez ohledu na jejich stav.  
- Vyberte případ kolekce přiřazené k odběrateli, nebo ponechejte toto pole prázdné. Pokud je vybrán případ, budou zobrazeny pouze transakce a aktivity, které jsou přidruženy k případu v tomto formuláři.  
5. Vyberte možnost **Zobrazit seznam**.
- Vyberte účet odběratele nebo ponechejte výchozí hodnotu. Ve výchozím nastavení se jedná o vybraný účet odběratele na stránce se seznamem nebo ve formuláři, ze kterého jste otevřeli tento formulář. Pokud jste formulář otevřeli ze stránky se seznam, odběratelé v seznamu jsou odběratelé, kteří jsou zahrnuti do fondu inkasa použitého na stránce se seznamem.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]