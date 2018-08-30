---
title: "Nastavení a práce s výstrahami u podvodů kontaktního střediska"
description: "Toto téma vysvětluje, jak nastavit pravidla výstrahy pro zástupce z oddělení služeb zákazníkům zaměřené na potenciálně podvodné informace při zpracování objednávek. Můžete definovat zvláštní kódy, které jsou automaticky nebo ručně použity k blokování podezřelých objednávek."
author: josaw1
manager: AnnBe
ms.date: 05/14/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: SalesPostingHistory, MCRHoldCodeTrans, SysOperationTemplateForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 6cca9e5b606f298d000354f6aeb01fbe2c8f2141
ms.contentlocale: cs-cz
ms.lasthandoff: 08/08/2018

---

# <a name="set-up-and-work-with-call-center-fraud-alerts"></a>Nastavení a práce s výstrahami u podvodů kontaktního střediska

[!include [banner](includes/banner.md)]

Toto téma vysvětluje, jak lze nastavit kritéria a pravidla pro blokování potenciálně podvodných prodejních objednávek do doby, než je zkontrolujete. Funkce kontroly podvodu se používá při ověřování platnosti informací na prodejní objednávce. Pokud se informace v prodejní objednávce zdají být pochybné na základě kritérií a pravidel organizace týkajících se podvodu, objednávku lze pozdržet pro další kontrolu. V takovém případě objednávku nelze uvolnit do skladu pro další zpracování, dokud nebude blokování vymazáno.

> [!NOTE]
> Tuto funkci lze použít pouze se zpracováním prodejních objednávek pro kanál kontaktního střediska Retail.

## <a name="turning-on-the-fraud-check-feature"></a>Zapnutí funkce pro zjišťování podvodů

Chcete-li použít funkci zjišťování podvodu, je nutné nastavit možnost **Povolit dokončení objednávky** na kanálu na **Ano**, když je kanál kontaktního střediska [definován](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/set-up-order-processing-options). Když je ukončení objednávky zapnuto, uživatelé kontaktního střediska musí zvolit **Dokončit** na stránce prodejní objednávky pro všechny prodejní objednávky, které jsou vytvořeny. Akce dokončení bude mít za následek otevření stránky **Souhrn prodejní objednávky**. Poté, co uživatelé zadají požadovaná data platby na stránce **Souhrn prodejní objednávky**, vyberou **Odeslat** pro dokončení objednávky. Při odeslání objednávky se spustí funkce zjištění podvodu a všechna pravidla, která jsou v systému aktivní, se automaticky ověří.

Uživatelé kontaktního střediska mohou také ručně blokovat prodejní objednávku ke kontrole proti podvodu, než zvolí **Odeslat**. Chcete-li ručně blokovat prodejní objednávku, na stránce **Souhrn prodejní objednávky** vyberte **Blokování** \> **Ruční blokování kvůli podvodu**. Poté budete vyzváni k zadání komentáře vysvětlujícího důvod blokování objednávky. Tato poznámka se zobrazí na pracovní ploše [blokování objednávek](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/work-with-order-holds), aby poskytla kontextu uživateli kontrolujícímu objednávky, které jsou blokované, a pomohla mu určit, zda má být objednávka uvolněna.

Kromě konfigurace možnosti **Povolit dokončení objednávky** na kanálu je nutné také nastavit funkci zjištění podvodu v parametrech kontaktního střediska. Přejděte na **Maloobchod** \> **Nastavení kanálu** \> **Nastavení kontaktního střediska** \> **Parametry kontaktního střediska**. Na stránce **Parametry kontaktního střediska** na kartě **Blokování** nastavte **Zjišťování podvodu** na **Ano**.

Na kartě **Blokování** byste měli také definovat [kódy blokování](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/work-with-order-holds), které budou použity pro objednávku, která je ručně nebo automaticky blokována kvůli kontrole proti podvodu. Nastavte kódy blokování v polích **Kód ručního blokování kvůli podvodu** a **Kód blokování kvůli podvodu**. Může být užitečné vytvořit dva jedinečné kódy blokování, aby uživatelé, kteří pracují na pracovní ploše blokování mohli snadno filtrovat a odlišit automatické blokování od ručního.

Aby kontrola proti podvodu fungovala účinně, je nutné nastavit také pole **Minimální hodnocení**. Každé kritérium podvodu a pravidlo, které jsou definované v systému, mají skóre. Když se prodejní objednávka kontroluje proti shodě podvodu a nalezne se jedna nebo více shod, skóre se sečtou a dají objednávce výsledné hodnocení proti podvodu. Pokud celkové hodnocení podvodu objednávky překračuje hodnotu pole **Minimální hodnocení**, objednávka se automaticky zablokuje. Volitelně můžete použít jiná pole související s hodnocením na kartě **Blokování**, abyste definovali hodnocení e-mailu, telefonu, PSČ a rozšířeného PSČ. Pokud nezadáte hodnocení pro žádné z těchto statických kritérií podvodu, když je definujete na stránce **Statická podvodná data**, systém je bude hodnotit pomocí výchozích hodnocení zadaných na kartě **Blokování** na stránce **Parametry kontaktního střediska**.

Nakonec použijte pole **Typ komentáře k podvodu** pro určení typu dokumentu, který má být použit tehdy, když uživatelé zadávají komentáře při ručním blokování objednávky za účelem kontroly proti podvodu. Nejčastěji je toto pole nastaveno na **Poznámka**.

## <a name="defining-fraud-criteria-and-rules"></a>Definování kritérií a pravidel podvodu

Systém poskytuje dva typy kritérií podvodu pro určení, zda má být objednávka pozdržena kvůli kontrole proti podvodu:

- **Statická podvodná data** používají určitou hodnotu, jako je například telefonní číslo, které bylo uvedeno na seznamu blokovaných čísel, nebo e-mailová adresa označená příznakem, protože je známo, že byly použity pro předchozí podvodné transakce. Chcete-li nastavit statická podvodná data, přejděte na **Maloobchodní** \> **Nastavení kanálu** \> **Nastavení kontaktního střediska** \> **Podvod** \> **Statická podvodná data**. Na stránce **Statická podvodná data** můžete přidat kritéria podvodu ručně nebo pomocí importu dat. Výsledky jsou připojeny k informacím o podvodu. Pokud je zapnuta kontrola podvodu, každá zadaná prodejní objednávka bude porovnána se statickými daty. Pokud se data nacházejí buď na fakturační adrese zákazníka, nebo na doručovací drese navázané na hlavičku objednávky, nebo pokud jsou data nalezena v dodacích adresách propojených s některým z řádků v této prodejní objednávce, skóre všech jedinečných shody se přidá dohromady a porovná s hodnotou **Minimální hodnocení** pro určení, zda má být objednávka zablokována.
- **Podvodná pravidla** se skládají z uživatelem definovaných proměnných a podmínek definovaných pro tyto proměnné. Chcete-li vytvořit pravidla, přejděte na **Maloobchod** \> **Nastavení kanálu** \> **Nastavení kontaktního střediska** \> **Podvod** \> **Pravidla**. Podvodná pravidla umožňují společnosti konfigurovat složitější sadu pravidel, která mohou obsahovat výrazy **AND** nebo **OR** pro vyhodnocení více podmínek. Uživatel chce například zablokovat kvůli kontrole proti podvodu všechny objednávky pro odběratele, kteří patří do určité skupiny odběratelů a kteří objednali konkrétní produkt. V tomto případě se definují podmínky k ověření odběratelů a produktů na stránce **Pravidla** pomocí podmínky AND. Objednávka je poté blokována pouze v případě, že jsou splněny obě podmínky, a pokud hodnota skóre přiřazená k tomuto pravidlu, plus hodnota skóre všech dalších pravidel, které objednávka naplní, způsobí, že celkové hodnocení podvodné objednávky překročí **Minimální hodnocení** definované na stránce **Parametry kontaktního střediska**.

> [!NOTE]
> Více pravidel nebo výrazně složitá pravidla způsobí špatný výkonu systému při odesílání prodejních objednávek. Funkce kontroly proti podvodu nebyla optimalizována pro zpracování velkého objemu statických datových položek týkajících se podvodu a mnoha aktivních pravidel. Mějte na paměti, že každé pravidlo se vyhodnocuje, když uživatelé zvolí **Odeslat** při zadávání prodejní objednávky. Pravidla jsou vyhodnocována proti záhlaví prodejní objednávky a všem řádkům objednávky. Čím více existuje pravidel a čím více složitější jsou výrazy pravidel, tím déle bude trvat zpracování. Pokud existuje velký počet položek řádku na objednávce a velký počet aktivních pravidel a položek statických dat, automatický proces přezkoumání a ověření všech dat a výpočtu skóre podvodu může mít dopad na výkon. Organizace používající tuto funkci by měly vždy otestovat a potvrdit, že doba zpracování pro odeslání objednávky je přijatelná, dříve než použijí změny pravidel nebo statických kritérií podvodu v produkčním prostředí.

## <a name="identifying-orders-that-are-on-hold-for-fraud-review"></a>Identifikace objednávek, které jsou blokované ke kontrole proti podvodu

Když uživatel kontaktního střediska odešle prodejní objednávku a objednávka odpovídá kritériím nebo pravidlům podvodu a skóre přesahuje minimum, uživatel dostane zprávu s upozorněním o tom, že objednávka byla blokována. Uživatelé mohou zavřít tuto zprávu, protože má pouze informativní charakter. Uživatelé mohou volitelně sdělit tyto informace odběrateli. Podnik by měl určit protokol, podle kterého mají uživatelé v této situaci postupovat.

Objednávka je uložena, a obsahuje příznak **Nezpracovávat**. Tento příznak pomáhá zajistit, aby objednávku nebylo možné uvolnit do skladu. Uživatelé mohou kdykoliv zobrazit nastavení příznaku **Nezpracovávat** pro každou prodejní objednávku na stránce **Podrobný stav**. Tuto stránku lze otevřít z e stránek **Všechny prodejní objednávky** a **Služby odběratele**. Systém také aktualizuje hodnotu pole **Podrobný stav** pro objednávku na **Blokování podvodu**.

Chcete-li zobrazit a spravovat objednávky, které jsou blokovány kvůli kontrole proti podvodu, přejděte na **Maloobchod** \> **Odběratelé** \> **Blokování objednávek**. Na stránce **Blokování objednávek** v seznamu vyberte položku a klikněte na **Blokování objednávky**, abyste viděli podrobnější zobrazení, které obsahuje informace o důvodu blokování. Na pevné záložce **Podrobnosti podvodu** můžete zobrazit systematická kritéria podvodu, která byla nalezena jako shoda pro objednávku a použité skóre. Pokud objednávka byla blokována ručně, můžete provést revizi všech komentářů zadaných uživatelem, který objednávku zablokoval pohledem do části **Poznámky o podvodu** na pevné záložce **Poznámky**.

Další informace o práci s blokováním objednávek najdete v části [Blokování objednávek](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/work-with-order-holds).

