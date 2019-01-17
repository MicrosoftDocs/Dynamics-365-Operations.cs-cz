---
title: "Plnění objednávek obchodu"
description: "Toto téma poskytuje přehled plnění objednávky obchodu."
author: rubencdelgado
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: rubencdelgado
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: b3eeda217e00b33962561bcb2ee6185275f52fe2
ms.contentlocale: cs-cz
ms.lasthandoff: 01/04/2019

---

# <a name="store-order-fulfillment"></a>Plnění objednávek obchodu

[!include [banner](includes/banner.md)]

Mnoho maloobchodních prodejců by chtělo optimalizovat plnění objednávky tak, že povolí plnění objednávky obchodům. Plnění objednávek na úrovni obchodu může pomoci zmírnit scénáře přeplnění pro konkrétní obchod, nebo může být zapotřebí z logistického hlediska v případech, kdy má obchod dodatečnou kapacitu nebo je umístěn v těsnější vzdálenosti od zákazníka. Aby se vyhovělo této potřebě, je na pokladním místě k dispozici sjednocená operace plnění objednávky.

Objednávky pro plnění v konkrétním obchodě mají sklad obchodu označený v záhlaví nebo řádcích objednávky.

Operace plnění objednávky na pokladním místě poskytuje jediný pracovní prostor v pokladním místě, který lze použít pro zpracování objednávek. To obsahuje vše, od přijetí objednávky až po její označení jako vyexpedované nebo inicializování vyzvednutí v obchodě.

## <a name="access-unified-order-fulfillment-in-the-point-of-sale"></a>Přístup k jednotnému plnění objednávky v pokladním místě

Plnění objednávky [ID operace 928](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-operations) lze použít pro přístup k pracovní oblasti plnění objednávky obchodu v pokladním místě.

Operace plnění objednávky nemá momentálně vlastní oprávnění, ale v budoucnosti budou uživatelé moci používat oprávnění **Povolit načtení objednávky** k vyvolání operace z pokladního místa.

Na úrovni obchodu je k dispozici nastavení konfigurace k určení, zda řádek objednávky musí být přijat ručně z pokladního místa. Pokud tato možnost konfigurace není nastavena, řádky objednávky budou přijaty ve výchozím nastavení. Pokud je tato možnost konfigurace zapnuta, uživatelé budou muset na pokladním místě zvolit oprávnění **Povolit přijetí objednávky** pro příjem objednávek z pokladního místa.

Řádky objednávky mohou být také odmítnuty z pokladního místa. Zamítnutí řádku objednávky znamená, že nebude plněna v obchodě, a odešle řádek objednávky zpět pro opětovné přiřazení do jiného obchodu nebo skladu. Oprávnění pro odmítnutí řádku objednávky, je udělováno prostřednictvím oprávnění **Povolit odmítnutí objednávky**.

## <a name="order-fulfillment-operation-parameters"></a>Parametry operace plnění objednávky

Plnění objednávky poskytuje okamžité parametry, které lze použít na operaci, když je volána na pokladním místě. Když je nakonfigurován parametr **Všechny objednávky**, všechny objednávky se zobrazí při použití operace. Parametr **Objednávky k expedici** zobrazuje jen objednávky, které musí být expedovány z obchodu, a parametr **Objednávky k výdeji** zobrazí objednávky, které budou vyzvednuty v obchodě.

## <a name="orders-for-fulfillment"></a>Objednávky k plnění

Operace plnění objednávky zobrazí pouze objednávky, které budou buď vyzvednuty v obchodě, nebo expedovány z aktuálního obchodu. Objednávky z jiných obchodů k plnění nejsou uvedeny při použití operace plnění objednávky.

## <a name="line-selection"></a>Výběr řádku

Řádky lze vybrat pomocí funkce **Vybrat** v podokně akcí. Když je povolena funkce **Vybrat**, lze vybrat ke zpracování několik řádků. Opětovným kliknutím na tentýž řádek můžete zvolené řádky vymazat.

## <a name="line-details"></a>Detaily řádku

Podrobnosti řádku lze zobrazit pomocí nabídky plovoucího panelu podrobností řádku. Při použití této nabídky jsou k dispozici tři karty k zobrazení dalších informací pro vybraný řádek. První karta **Podrobnosti řádku** zobrazuje podrobnosti samotného řádku, jako je například objednané a zbývající množství. Jsou uvedeny i další podrobnosti, včetně vyskladněného, zabaleného a fakturovaného množství, stejně jako způsob doručení a adresa doručení. Karta **Podrobnosti objednávky** obsahuje informace záhlaví objednávky, včetně odběratele, ID odběratele, číslo objednávky, celkovou hodnot objednávky a zůstatek. Karta **Zásoby** zobrazuje informace pro vybraný řádek s ohledem na dostupné fyzické zásoby, rezervované zásoby a objednané zásoby.

Pokud je vybráno více řádků, nabídka plovoucího panelu podrobností řádku objednávky pouze označí, že je zvoleno více řádků. Chcete-li zobrazit podrobné informace o jednotlivých řádcích, vymažete řádky, dokud nezůstane pouze jeden řádek.

## <a name="pending-order-lines"></a>Čekající řádky objednávky

Sjednocené plnění objednávky zahrnuje možnost ručního přijetí objednávky. Standardně jsou objednávky k plnění v obchodě již přijaty. Pokud však obchodní procesy určují, že pracovník na úrovni obchodu musí přijmout objednávky, lze ruční přijetí zapnout na úrovni maloobchodu. Chcete-li povolit přijetí objednávky, přejděte na **Maloobchod** \> **Kanály** \> **Maloobchody** \> **Všechny maloobchody**. Otevřete požadovaný obchod a na kartě **Obecné** vyhledejte dílčí záhlaví **Plnění objednávky**. Toto dílčí záhlaví má možnost **Ruční přijetí**, která je nastavena na **Ne** ve výchozím nastavení. Nastavením této možnosti na **Ano** a synchronizací změn do databáze kanálů mohou řádky objednávky projít procesem přijetí.

Pracovníci s oprávněním **Povolit přijetí objednávky** mohou otevřít plnění objednávky a vybrat řádky k přijetí. Po přijetí řádků se jejich stav změní z **Čekající** na **Přijato** a zbývající část procesu plnění objednávky může pokračovat. Když je zapnuto **Ruční přijetí**, objednávky nebudou zpracovány, dokud nebudou přijaty.

Objednávky pro vyzvednutí v obchodě nemají nikdy stav **Čekající**. To proto, aby nedošlo ke scénáři, ve kterém odběratel dorazí do obchodu a řádek objednávky nelze zpracovat, protože není k dispozici pracovník s dostatečným oprávněním.

## <a name="accepted-order-lines"></a>Přijaté řádky objednávky

Objednávky se stavem řádku **Přijato** mohou pokračovat procesem plnění objednávky na pokladním místě. Po přijetí objednávky lze provést veškeré zbývající akce proti řádku objednávky.

Například přijatý řádek objednávky lze vybrat a poté vydat přímo bez nutnosti procházet výdejem a balením.

## <a name="line-actions"></a>Akce řádku

### <a name="pick"></a>Vyskladnit

Kategorie akcí **Vyskladnit** je poskytnuta pro usnadnění procesu výdeje řádků objednávky z police. Akci výdeje lze provést pouze na řádcích objednávky, které již byly dříve přijaty.

**Akce: výdej**

- **Výsledný stav POS:** výdej
- **Výsledný stav účetního systému:** beze změny

Po přijetí objednávky lze vybrat řádky a označit je jako **Výdej**. Označení řádku jako **Výdej** slouží k označení, že práce výdeje již probíhá na řádku. Tím zabráníte dvěma pracovníků v pokusu vydat stejné řádky objednávky současně.

**Akce: Tisk výdejky**

- **Výsledný stav:** výdej
- **Výsledný stav účetního systému:** beze změny

Výdejky lze vytisknout na pokladním místě, aby se pomohlo pracovníkům při provádění procesu výdeje. Vytištěnou výdejku může mít u sebe pracovníka provádějící výdej, a jakmile jsou produkty vydány, pracovníka je ručně označí na výdejce jako vyskladněné.

Formát výdejky je nakonfigurován v aplikaci Dynamics 365 for Retail a přidán do profilu příjemek. Další informace o nastavení profilů příjemek naleznete v tématu [Šablony pro příjemky a tisk](https://docs.microsoft.com/dynamics365/unified-operations/retail/receipt-templates-printing).

Jestliže jsou vybrané řádky a u těchto řádků se vytiskne výdejka, jsou automaticky aktualizovány se stavem **Výdej**.

**Akce: Označit jako vyskladněno**

- **Výsledný stav:** Vyskladněno nebo částečně vyskladněno
- **Výsledný stav v účetním systému:** Vyskladněno nebo částečně vyskladněno

Poté, co bylo provedeno fyzické vyskladnění, lze řádky označit jako **Vyskladněno**. Výběrem řádku a jeho označením stavem **Vyskladněno** provedete volání v reálném čase k aktualizaci řádku objednávky v aplikaci Dynamics 365 for Retail. Poté, co byl řádek označen jako **Vyskladněno** na pokladním místě, je také aktualizován stav v účetním systému na **Vyskladněno** a skladové transakce budou odrážet to, že určené množství bylo sníženo.

Při zpracování objednávek v čase můžete pro konkrétní řádek zpracovat částečná množství. Pokud je vybrán řádek a je provedena akce **Označit jako vyskladněné**, a množství jě větší než jedna, bude uživatel vyzván k množství. Zbývající množství k výdeji je vyplněno automaticky. Je-li určeno množství menší než zbývající, stav řádku se změní na **Částečně vyskladněno**. Když je v účetním systému aktualizován řádek objednávky, bude to také odrážet stav částečného vyskladnění, a množství zadané uživatelem se použije pro aktualizaci skladu.

Pokud je řádek objednávky vyskladněn s chybou, je nutné provést na řádku objednávky v účetním systému proces naskladnění. Pokladní místo momentálně nepodporuje žádnou akci naskladnění.

Řádky objednávky z jiné objednávky lze vybrat a označit jako **Výdej**, vytisknout je na stejnou výdejku nebo označit jako **Vyskladněno**.

### <a name="pack"></a>Balení

Řádky objednávky lze zabalit kdykoli po přijetí řádku objednávky.

**Akce: Vytisknout dodací list**

- **Výsledný stav:** Zabaleno nebo částečně zabaleno
- **Výsledný stav v účetním systému:** Dodáno nebo částečně dodáno

Tato akce označí řádky jako zabalené nebo částečně zabalené a vytiskne dodací list. Dodací list lze vytisknout pro ověření produktů, které jsou zabaleny dohromady. Formát dodacího listu je nakonfigurován v aplikaci Dynamics 365 for Retail a přidán do profilu příjemek. Další informace o nastavení profilů příjemek naleznete v tématu [Šablony pro příjemky a tisk](https://docs.microsoft.com/dynamics365/unified-operations/retail/receipt-templates-printing).

**Akce: Označit jako zabaleno**

- **Výsledný stav:** Zabaleno nebo částečně zabaleno
- **Výsledný stav v účetním systému:** Dodáno nebo částečně dodáno

Akci **Označit jako zabaleno** lze použít k označení, že řádky jsou zabaleny bez tisku dodacího listu. Obě možnosti **Tisk dodacího listu** a **Označit jako zabaleno** mají za následek skladové transakce v účetním systému. Dodací listy na pokladním místě budou mít za následek vygenerování deníků dodacích listů v účetním systému.

Pokud je řádek objednávky zabalen chybně, deník dodacích listů musí být opraven v účetním systému.

Současně lze zabalit pouze řádky na stejné objednávce a se stejným způsobem dodání.

V současné době je možnost označit řádky vyzvednutí v obchodě jako **Zabaleno** zakázána. Tato možnost bude přidána v budoucí verzi. Proces vytvoření dodacího listu bude rozšířen, aby podporoval vložení informace o dodání třetí strany do procesu dodacího listu.

### <a name="pick-up"></a>Vyzvednutí

Objednávky pro vyzvednutí v obchodě lze vydat přímo, jakmile jsou načteny v pokladním místě. Objednávky pro vyzvednutí v obchodě nepodléhají přijetí.

**Akce: Výdej**

- **Výsledný stav:** Fakturováno nebo částečně fakturováno
- **Výsledný stav v účetním systému:** Fakturováno nebo částečně fakturováno

Když je řádek vybrán pro výdej z jednotného plnění objednávky, celá objednávka je načtena do pokladního místa a je označeno celé množství pro vybraný řádek. Ostatní řádky objednávky jsou rovněž načteny do zobrazení transakce pokladního místa, ale množství je označeno jako nula.

Jakmile jsou načteny řádky pro výdej do zobrazení transakce, transakci lze uhradit obvyklým způsobem.

Řádky, které byly plně vyfakturována prostřednictvím výdeje, se již nebudou zobrazovat ve sjednoceném zpracování objednávky. Řádky, které byly vydány částečně, se budou nadále zobrazovat ve sjednoceném plnění objednávky, dokud nebudou vydány úplně.

Pokud je řádek vyskladněn chybně, je nutné se vrátit a chybu opravit.

Současně lze vydat pouze řádky na stejné objednávce a se stejným způsobem dodání.

### <a name="shipping"></a>Expedice

Řádky objednávky, které mají být expedovány z obchodu, mohou být zpracovány prostřednictvím sjednoceného plnění objednávky pomocí akce **Expedovat**. Je-li ruční přijetí řádku objednávky nakonfigurováno na úrovni kanálu, objednávky musí být přijaty před odesláním. Jakmile je řádek objednávky přijat a má stav **Čekající** nebo jiný stav, lze řádky expedovat.

**Akce: Expedovat**

- **Výsledný stav:** Fakturováno nebo částečně fakturováno
- **Výsledný stav v účetním systému:** Fakturováno nebo částečně fakturováno

Řádky expedované ze sjednoceného plnění objednávky jsou fakturovány z účetního systému podobně, jako když je objednávka fakturována přímo z účetního systému. Řádky expedované ze sjednoceného plnění objednávky nejsou načteny do zobrazení transakce a v době expedice řádků není provedeno žádné uhrazení.

Řádky objednávky, které byly plně dodány, se již nezobrazí ve sjednoceném plnění objednávky. Řádky, které byly expedovány částečně, se budou nadále zobrazovat ve sjednoceném plnění objednávky, dokud nebudou expedovány úplně.

Pouze řádky ze stejné objednávky lze expedovat současně. Pokud mají řádky ze stejné objednávky různé způsoby dodání, mohou být vybrány stále pro expedici současně.

### <a name="reject"></a>Zamítnout

Řádky nebo částečné řádky lze odmítnout. To umožňuje jejich opětovné přiřazení z účetního systému do jiného obchodu nebo skladu. Řádky lze zamítnout pouze tehdy, pokud nebyly ještě vyskladněny či zabaleny. Chcete-li odmítnout řádek, který byl vyskladněn nebo zabalen, musí být u toho řádku zrušeno vydání nebo zabalení z účetního systému.

**Action: Odmítnout**

- **Výsledný stav:** Odmítnuto
- **Výsledný stav účetního systému:** beze změny

Odmítnuté řádky objednávky lze zobrazit z pracovního prostoru **Zpracování a dotaz na prodejní objednávku**. Vymažte osobní filtr v pracovním prostoru, abyste zobrazili všechny odmítnuté řádky objednávky mezi obchody. Karta **Odmítnuté řádky objednávky** pod částí **Objednávky a oblíbené** zobrazuje podrobnosti řádku objednávky. Uživatelé mohou také kliknout na tlačítko **Odmítnuté řádky objednávky** pod částí **Souhrn** a přejít na zobrazení prodejní objednávky. Zobrazí se všechny objednávky, které mají nejméně jeden odmítnutý řádek. Jestliže je povolena distribuovaná správa objednávky, budou tyto odmítnuté objednávky automaticky znovu přiřazeny do příslušných obchodů pro plnění. Tyto řádky objednávky lze však též znovu přiřadit ručně. To provedete výběrem řádku, který zobrazuje **Stav plnění** jako **Odmítnuto** a změnou pracoviště/skladu podle potřeby. Klikněte na rozevírací nabídku **Aktualizovat řádek** a klikněte na **Resetovat stav plnění** ke změně stavu plnění z **Odmítnuto** na **Přijato** nebo **Čekající**, v závislosti na nastavení plnění objednávky. Po resetování stavu plnění budou moci pracovníci obchodu zobrazit řádky objednávky v POS.

## <a name="line-quantity-tracking"></a>Sledování množství řádku

Jeden řádek objednávky s množství větším než jedna lze zpracovat v čase, což má za následek více dílčích stavů řádků objednávky. Například pokud má stavitel projekt, který vyžadoval 500 desek, ale vyzvedne si nebo mu je doručeno pouze několik desek současně v průběhu projektu, mohou být množství, která jsou současně vydána, zabalena a expedováno.

Kdykoli je řádek vybrán, zbývající množství pro řádek bude automaticky vyplněn, a předpokládá se, že zbývající množství se zpracovává. Když použijeme výše uvedený příklad, tak pokud bylo vyskladněno již 200 desek a je vybrán řádek desek pro výdej, bude automaticky vyplněno zbývající množství 300 v množství. To samé platí tehdy, pokud bylo 200 desek již fakturováno. Zbývající množství v takovém případě bude vyplněno automaticky.

Pokračujeme-li v uvedeném příkladu, tak pokud je 200 desek je označeno jako zabalených a je zvolena expedice, bude automaticky vyplněno celé množství 500. Pokud je expedováno pouze 200 desek, systém bude předpokládat, že dříve zabalené desky jsou expedovány a zabalené množství bude sníženo. Pokud je expedováno 201 desek, zabalené desky jsou nejprve sníženy o zbývající jednu desky ze zbývajícího množství.

## <a name="line-statuses"></a>Stavy řádku 

Řádky objednávky v pokladním místě mají několik stavů, aby odrážely stav řádků objednávky. Ve všech případech se neshodují stavy v pokladním místě a v účetním systému. Stav řádku objednávky lze zobrazit prostřednictvím pokladního místa pomocí operací plnění objednávky. V účetním systému lze zobrazit řádky objednávky z podrobností o objednávce. K podrobnostem objednávky lze přistupovat prostřednictvím možností **Maloobchod** \> **Odběratelé** \> **Všechny objednávky odběratele**. Pro zobrazení podrobností o objednávce vyberte **ID objednávky**. Z podrobností o objednávce vyberte kartu **Prodejní objednávka** a potom vyberte **Podrobný stav** pod dílčím záhlavím **Zobrazit**.

- **Čekající** - Řádky objednávky, které byly přiřazeny k obchodu, ale dosud nebyla přijaty, mají stav **Čekající** při zobrazení v pokladním místě. Řádky čekající na přijetí na pokladním místě budou mít v účetním systému stav **Zpracování objednávky**.
- **Přijato** – Řádky objednávky, které byly přijaty ručně nebo automaticky, budou mít stav **Přijato** při zobrazení v pokladním místě. Řádky se stavem **Přijato** se zobrazí v účetním systému jako **Zpracování objednávky**.
- **Výdej** – Řádky, které jsou aktuálně vyzvedávány na úrovni obchodu, mají stav **Výdej**. Tytéž řádky při zobrazení v účetním systému se zobrazují jako **Zpracování objednávky**.
- **Vyskladněno** a **Částečně vyskladněno** – řádky, které byly vyskladněny nebo částečně vyskladněny na pokladním místě, budou mít stav **Vyskladněno** nebo **Částečně vyskladněno**. Stejné řádky v účetním systému se zobrazí také jako **Vyskladněno** nebo **Částečně vyskladněno**.
- **Zabaleno** a **Částečně zabaleno** – řádky, které byly zabaleny nebo částečně zabaleny na pokladním místě, budou mít stav **Zabaleno** nebo **Částečně zabaleno**. Stejné řádky v účetním systému se zobrazí také jako **Dodáno** nebo **Částečně dodáno**.
- **Částečně fakturováno** – řádky, které bylo částečně vyzvednuty nebo částečně vyexpedovány, budou mít stav **Částečně fakturováno** na pokladním místě a v účetním systému.
- **Fakturováno** – řádky, které byly plně vyfakturovány na pokladním místě, se již nebudou zobrazovat k plnění. V účetním systému je stav pro tyto řádky **Fakturováno**.

## <a name="order-fulfillment-filtering"></a>Filtrování plnění objednávek

Plnění objednávky na pokladním místě obsahuje filtrování umožňující uživateli snadné vyhledávání podle potřeb. Filtry lze změnit ve spodní části podokna akcí na obrazovce **Pokladní místo**. Ve výchozím nastavení je použit filtr **Typ dodání**, podle nastavení operace. Je-li operaci nastavena s parametrem **Všechny objednávky**, pak se daný filtr použije při přístupu k plnění objednávky. To platí i pro parametry **Vyzvednutí v obchodě** a **Expedovat z obchodu**. Jiné filtry, které lze použít k zobrazení plnění objednávky, zahrnují:

- Název zákazníka
- Jméno zákazníka
- E-mail odběratele
- Číslo objednávky
- Způsob dodání
- Číslo příjemky
- ID odkazu na kanál
- Původní číslo obchodu
- Stav řádku
- Vytvořeno
- Datum dodání
- Datum příjmu

