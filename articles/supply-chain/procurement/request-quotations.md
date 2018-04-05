---
title: "Požadavky na nabídku"
description: "Toto téma obsahuje přehled požadavků na nabídku. Organizace vygenerují požadavek na nabídku v případě, že chtějí získat konkurenční nabídky od několika dodavatelů, týkající se zboží nebo služeb, které musí nakoupit."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchRFQCaseTable, PurchRFQCaseTableListPage, PurchRFQCompare, PurchRFQReplyTable, PurchRFQVendReplyTableListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 2154
ms.assetid: 3936996e-d943-46ca-8385-84c042990f1d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: b86363004b8702d1a654f2a1da49bba82fc8ff2a
ms.contentlocale: cs-cz
ms.lasthandoff: 03/26/2018

---

# <a name="requests-for-quotation-rfqs"></a>Požadavky na nabídku

[!include[banner](../includes/banner.md)]

Toto téma obsahuje přehled požadavků na nabídku. Organizace vygenerují požadavek na nabídku v případě, že chtějí získat konkurenční nabídky od několika dodavatelů, týkající se zboží nebo služeb, které musí nakoupit. V požadavku na nabídku požádejte dodavatele o zadání cen a dodacích lhůt pro zadané množství položek. Lze také požádat dodavatele, aby určili, zda budou účtovány vedlejší náklady, například přepravní náklady nebo slevy pro velké objednávky či včasnou platbu za fakturu dodavatele.

Proces požadavků na nabídku se skládá z následujících úloh:

1. Vytvoření a odeslání požadavku na nabídku jednomu nebo více dodavatelům.
2. Příjem a zaznamenání odpovědí na požadavek na nabídku (nabídky).
3. Převod přijatých nabídek na nákupní objednávky, nákupní smlouvu nebo nákupní žádanku.

Následující obrázek přehledně znázorňuje průběh procesu požadavku na nabídku.

[![Proces RFQ](./media/rfq-process-458x1024.jpg)](./media/rfq-process.jpg)

Požadavek na nabídku můžete vytvořit z plánovaných objednávek, z nákupní žádanky nebo ručním zadáním. Požadavek na nabídku, který vytvoříte, se nazývá případ požadavku na nabídku. Případ požadavku na nabídku je základní dokument, který použijete k vystavení požadavku na nabídku pro každého dodavatele.

Po přípravě případu požadavku na nabídku a přidání dodavatele zvolte v případu požadavku na nabídku **Odeslat**. Deník požadavku na nabídku se vygeneruje pro každého dodavatele, kterému jste odeslali požadavek na nabídku. Můžete nakonfigurovat nastavení správy tisku pro akci Odeslat, aby se buď vytiskla sestava pro každého dodavatele do archivu nebo odeslala sestava na e-mailovou adresu každého dodavatele. Deník požadavku na nabídku pro každého dodavatele lze navíc použít k vytvoření sestavy, kterou lze odeslat nebo později znovu odeslat dodavateli. Také můžete nakonfigurovat akci Odeslat, aby se vygeneroval list odpovědí, který mohou dodavatelé vyplnit.

V tomto tématu je popsán postup zpracování požadavku na nabídku, když se nepoužívá dodavatelská spolupráce. Je-li váš systém nastaven pro dodavatelskou spolupráci, dodavatelé mohou zadat nabídky přímo do aplikace Microsoft Dynamics 365 for Finance and Operations. Další informace naleznete v tématu [Dodavatelská spolupráce se zákazníky](vendor-collaboration-work-customers-dynamics-365-operations.md).
 
Pokud musíte změnit požadavek na nabídku po jeho odeslání, můžete opět odeslat požadavek na nabídku dodavatelům po jeho dokončení s použitím dvou akcí úprav: Vytvoření a Dokončení.

Jakmile obdržíte nabídky e-mailem, je nutné je zadat na stránce **Odpovědi na požadavky na nabídku**. Pokud jste vybrali možnost **Kopírovat data do odpovědi**, data jako například množství a data z případu požadavku na nabídku jsou zkopírovány do odpovědi na nabídku. Tato data lze změnit podle nabídky dodavatele.

Pokud je druhá iterace odpovědi vyžadována pro určitého dodavatele, zvolte **Vrácení** na stránce **Odpověď na požadavek na nabídku**. Akce Vrácení vytvoří nový deník a sestavu, která bude vytištěna, archivována a odeslána podle nastavení správy tisku.

Pokud jste přidali kritéria hodnocení do případu požadavku na nabídku, odpověď požadavku na nabídku bude mít panel hodnocení, kde můžete zadat výsledky. Celkové hodnocení se zobrazí při porovnání odpovědí na stránce **Porovnat odpovědi**. Na této stránce můžete také porovnat jiná data odpovědi, například řádkovou cenu, datum dodání a celkovou cenu.

Poté, co si vyberete nabídku nebo dílčí nabídky, můžete je přijmout a odmítnout ostatní. Vygenerují se deníky přijetí, deníky odmítnutí a příslušné sestavy a budou vytištěny, archivovány a odeslány podle nastavení správy tisku. Při přijetí nabídky nebo konkrétních řádků v nabídce bude vytvořena nákupní smlouva nebo nákupní objednávka nebo aktualizován nákupní požadavek, v závislosti na typu nákupního požadavku na nabídku. Můžete vytvořit obchodní smlouvu, kterou můžete později použít u všech odpovědí, bez ohledu na to, zda jste je přijali nebo zamítli.

Stav požadavku na nabídku se zobrazí v záhlaví požadavku na nabídku a závisí na stavu řádků požadavku na nabídku. Stav označuje, do jaké míry byl zpracován požadavek na nabídku. Každý požadavek na nabídku má dvě hodnoty stavu: nejnižší a nejvyšší stav. Nejnižší stav je nejméně pokročilou fází jakékoli řádky v požadavku na nabídku a nejvyšší stav je nejpokročilejší fází jakékoli řádky v požadavku na nabídku. Pokud je například poslední pokročilá fáze v požadavku na nabídku určena pro řádku, která byla vytvořena, bude nejnižší fáze požadavku **Vytvořeno**. Pokud je nejpokročilejší fáze v požadavku na nabídku určena pro řádku, která byla odeslána dodavatelům, bude její nejvyšší stav **Odesláno**. Stavy jsou automaticky aktualizovány při zpracování požadavku na nabídku.

Nejnižší a nejvyšší stav záhlaví požadavku na nabídku můžete zobrazit na stránce **Všechny požadavky na nabídky**. Nejnižší a nejvyšší stav řádku požadavku na nabídku můžete zobrazit na kartě **Řádky** na stránce **Požadavky na nabídky**.

Pořadí stavů zpracování požadavku na nabídku vypadá takto:

1. **Vytvořeno**
2. **Odesláno**
3. **Přijato**
4. **Přijato**, **Zrušeno** nebo **Odmítnuto**

Tyto stavy budou popsány podrobněji dále v tomto tématu.

## <a name="setting-up-rfq-functionality"></a>Nastavení funkce RFQ

Než bude možné vytvořit případ požadavku na nabídku, je nutné konfigurovat informace o požadavku na nabídku na stránce **Parametry modulu Zásobování a zdroje**. Při vytváření případu požadavku na nabídku lze zadat výchozí hodnoty, které budou zkopírovány do požadavku na nabídku. Můžete zadat následující výchozí hodnoty:

- Typ nákupu nového požadavku na nabídku: **Nákupní objednávka** nebo **Nákupní smlouva**
- Datum a čas vypršení platnosti
- Informace o dodání a platební podmínky
- Pole, která mají být zahrnuta v odpovědi na požadavek na nabídku

Tyto hodnoty lze přepsat pro konkrétní případ požadavku na nabídku.

Také je třeba nakonfigurovat proces změn. V rámci této konfigurace můžete zapnout blokování pole. Pokud je zapnuto uzamčení pole, musí zásobovací pracovník, který chce změnit požadavek na nabídku, nejprve zvolit **Vytvořit** v části **Dodatek** na záložce **Nabídka**. Poté, co byl požadavek na nabídku aktualizován dodatkem, musí zásobovací pracovník dokončit proces volbou možnosti **Dokončit**. Akce Dokončit vytvoří e-mailovou zprávu, která upozorní dodavatele na doplněný požadavek na nabídku.

Vyberte šablonu, která se má použít pro oznámení e-mailem odeslané dodavatelům na stránce **Parametry modulu Zásobování a zdroje**. Po vytvoření šablona může obsahovat následující náhradní tokeny:

- %Případ požadavku na nabídku%
- %Důvod pro vrácení nabídky%
- %Důvod pro dodatek%
- %Pořizovatel dodatku%
- %Společnost%
- %Název případu požadavku na nabídku%
- %Datum a čas vypršení platnosti%
- %Datum%

Tokeny %Důvod pro vrácení nabídky% a %Důvod pro dodatek% jsou nahrazeny textem, který pracovník zásobování může zadat po dokončení dodatku v průvodci **Dodatek**. Hodnoty pro token %Pořizovatel dodatku% a %Společnost% jsou automaticky převzaty z požadavku na nabídku. Token %Date% je nahrazen aktuálním datem.

Pokud zrušíte požadavek na nabídku poté, co byl odeslán, vyžaduje se též šablona e-mailu. Tato šablonu e-mailu se používá k odeslání oznámení o zrušení kontaktní osobě dodavatele. Je nutné vybrat šablonu na stránce **Parametry modulu Zásobování a zdroje**. Po vytvoření šablony může šablona obsahovat následující náhradní tokeny:

- %Důvod zrušení%
- %Případ požadavku na nabídku% 
- %Požadavek na nabídku zrušil/a%
- %Společnost%
- %Název případu požadavku na nabídku%
- %Datum%

Token %Důvod zrušení % se nahradí textem, který může zásobovací pracovník zadat v průvodci **Zrušení**. Token %Date% je nahrazen aktuálním datem.

Pokud chcete použít kódy důvodu u odpovědi na požadavek na nabídku a označit tak, proč nabídka byla zamítnuta nebo přijata, musíte nastavit kódy důvodu na stránce **Dodavatel – důvody**.

Vzhled vytištěných a uložených dokumentů požadavku na nabídku můžete nakonfigurovat na stránce **Nastavení formuláře** v modulu Zásobování a zdroje.

> [!NOTE]
> U konfigurace veřejného sektoru musíte použít procesu dodatku ke změně požadavku na nabídku, který již byl odeslána. Po odeslání požadavku na nabídku jsou pole uzamčena. Chcete-li tedy provést změny požadavku na nabídku, je nutné vybrat možnost **Vytvořit** pro zahájení procesu dodatku, jak bylo popsáno výše. Chování uzamčení je ovládáno možností **Zamknout požadavky na nabídku při odeslání** na stránce **Parametry modulu Zásobování a zdroje**. Ve výchozím nastavení je tento parametr nastaven na **Ano** a pro konfiguraci veřejného sektoru toto výchozí nastavení nelze změnit. Z toho vyplývá, že ačkoliv proces dodatku lze zpracovat ručně v konfiguraci neveřejného sektoru, je nutné ho použít pro konfiguraci veřejného sektoru.

Při vytváření požadavku na nabídku pro nákupní objednávku a přidávání skladových položek do požadavku na nabídku bude vytvořena také skladová transakce, která má stav příjmu **Příjem nabídky**. Při výpočtu zásob pomocí hlavního plánu jsou použity pouze řádky požadavku na nabídku tohoto stavu. Pokud chcete, aby hlavní plán zahrnoval řádky požadavku na nabídku jako očekávaný příjem, je nutné konfigurovat toto chování v nastavení hlavního plánování.

Správce nebo zástupce nákupu může vytvořit a spravovat typy oslovení, aby splňovaly požadavky zásobování organizace. Každý typ oslovení může být přidružen k metodě hodnocení. Metody hodnocení obsahují sadu kritérií, kterou lze použít, pokud dosáhnete úspěšné nabídky. Je nutné nastavit typy oslovení, metody hodnocení a kritéria hodnocení na stránce **Typ oslovení** a **Metoda hodnocení**.

## <a name="creating-and-sending-an-rfq"></a>Vytvoření a odeslání požadavku na nabídku

Vytvořte požadavek na nabídku, vyberte dodavatele, který má zadat nabídku k požadavku na nabídku a odešlete požadavek na nabídku dodavatelům. Správu tisku můžete použít pro směrování sestavy požadavku na nabídku a listu odpovědí do upřednostňovaného cíle.

Můžete vytvořit požadavek na nabídku nákupního typu **Nákupní objednávka** nebo **Nákupní smlouva**.

Pokud je požadavek na nabídku typu **Nákupní objednávka**, dojde k následujícímu chování:

- Při vytvoření řádků požadavku na nabídku se vytvoří skladové transakce, které mají stav příjmu **Příjem nabídky**.
- Při přijetí nabídky je vygenerována nákupní objednávka.

Pokud je požadavek na nabídku typu **Nákupní smlouva**, dojde k následujícímu chování:

- Požadavek na nabídku se používá pro dohodu o nákupu určitého množství nebo hodnoty produktu během času. Musíte vybrat rozsah dat, který se týká nákupní smlouvy a jména osoby, která spravuje nákupní smlouvu.
- Při přijetí nabídky je vygenerována nákupní smlouva.

Je-li požadavek na nabídku generován na základě nákupního požadavku, typ **Nákupní žádanka** je automaticky přiřazen. Nelze vytvořit ručně požadavek na nabídku typu **Nákupní žádanka**.

Požadavek na nabídku z nákupního požadavku můžete vytvořit pouze v případě, že je stav nákupního požadavku **Probíhá kontrola** a že jste přiřazeni k provádění další úlohy workflowu. Řádky nákupního požadavku se automaticky aktualizují, jakmile přijmete řádky z odpovědí na požadavky na nabídku (nabídky), které jste získali od dodavatelů. Pokud probíhá zpracování RFQ, nelze provést žádné akce nákupní žádanky (například dokončení, odmítnutí nebo schválení).

Pokud vytvoříte požadavek na nabídku, můžete vybrat typ oslovení. Typ oslovení určuje sadu kritérií hodnocení, která se používá k získání odpovědí na požadavky na nabídku.

K případu požadavku na nabídku můžete přiřadit dotazník. Tento dotazník se objeví na všech odpovědích po odeslání požadavku na nabídku.

Máte na výběr tři způsoby, jak vybrat dodavatele a přidat jej k případu požadavku na nabídku:

- Přidání dodavatelů po jednom.
- Vyhledání všech dodavatelů, které splňují konkrétní kritéria.
- Automatické přidání všech dodavatelů, kteří byli schváleni pro kategorie zásobování, které se používají v řádcích požadavku na nabídku.

Jakmile je případ požadavku na nabídku připraven, zvolte **Odeslat**. Akce Odeslat vytvoří deník a sestavy, které budou vytištěny, archivovány a odeslány podle nastavení správy tisku.

Pokud jste nastavili pole **Použít dodavatele pro přepočítávání cen** a **Použít informace o položce specifické pro dodavatele** na **Ano** na stránce **Odesílání požadavku na nabídku**, když jste odeslali požadavek na nabídku dodavatelům, některé informace pro konkrétní dodavatele budou automaticky doplněny. Tyto informace můžete upravit na stránce **Odpověď požadavku na nabídku**.

Následující tabulka uvádí změny stavu požadavku na nabídku při vytvoření nabídky a jejím odeslání dodavatelům.

| Akce                             | Nejnižší stav záhlaví požadavku na nabídku | Nejvyšší stav záhlaví požadavku na nabídku                        | Nejnižší stav řádky požadavku na nabídku | Nejvyšší stav řádky požadavku na nabídku |
|------------------------------------|--------------------------|--------------------------------------------------|------------------------|-------------------------|
| Vytvoření záhlaví RFQ a řádku.    | Vytvořeno                  | Vytvořeno                                          | Vytvořeno                | Vytvořeno |
| Odešlete požadavek na cenovou nabídku konkrétního dodavatele. | Odesláno                     | Odesláno                                             | Odesláno                   | Odesláno |
| Přidejte jiného dodavatele.                | Vytvořeno                  | Odešlete (požadavek na nabídku byl zaslán pouze jednomu dodavateli.) | Vytvořeno                | Odesláno |
| Odešlete požadavek na nabídku druhému dodavateli. | Odesláno                     | Odesláno                                             | Odesláno                   | Odesláno |

> [!NOTE]
> Do požadavku na nabídku můžete kdykoli přidat další dodavatele a nejnižší a nejvyšší stav se aktualizuje podle nových dodavatelů. Pokud jste například přijali nabídky od všech dodavatelů a přijali alespoň jeden řádek v nabídce, bude nejnižší stav v hlavičce požadavku na nabídku **Odmítnuto** a nejvyšší stav **Přijato**. Pokud přidáte nového dodavatele, bude nejnižší stav v jakémkoli řádku **Vytvořeno**. Nejnižší stav v záhlaví požadavku na nabídku se tedy aktualizuje na **Vytvořeno** a nejvyšší zůstane **Přijato**.

## <a name="amending-an-rfq"></a>Změna požadavku na nabídku

V některých případech je nutné požadavek na nabídku změnit po odeslání. Může být zapotřebí změnit požadavek na nabídku, například v případě, kdy byla změněna data dodání, nebo když požadujete další výrobky nebo jiné množství produktů. Proces dodatku můžete nakonfigurovat tak, aby bylo omezení větší nebo menší.

Pokud konfigurujete proces dodatku tak, aby byl více omezující, před úpravou polí v případu požadavku na nabídku, která již byla odeslán, je nutné vybrat **Vytvořit** v případu požadavku na nabídku pro zahájení dodatku. Po dokončení změn je nutné zvolit **Dokončit**. Poté bude provedeni procesem přidání informací pro e-mail, který bude odeslán pro upozornění dodavatelů na změnu. Aktualizovaná sestava požadavku na nabídku, která zahrnuje poznámku o změně, je automaticky přiřazena k e-mailu.

Pokud nakonfigurujete proces dodatku tak, aby byl méně omezující, nemusíte zvolit **Vytvořit** předtím, než bude možné upravit pole v případu požadavku na nabídku, který již byl odeslán. Musíte však ručně přidat poznámku o změně do požadavku na nabídku a odeslat případ znovu. Počítejte s tím, že tento přístup lze použít pouze v případě, že žádná z odpovědí (nabídek) nebyla upravována. Pokud jste zadali odpověď a je ve stavu **Přijato**, tlačítko **Odeslat** není k dispozici. V takovém případě je nutné vybrat **Vytvořit** a pak **Dokončit**, jako to musíte provést ve více omezujícím procesu. Odpověď se potom resetuje, aby odrážela změny případu požadavku na nabídku. 

Pokud dodavatelé používají rozhraní dodavatelské spolupráce k zadávání nabídek, musíte vždy použít proces dodatku, abyste informovali dodavatele o změnách případu požadavku na nabídku. Tento požadavek pomáhá zabránit situaci, kdy dodavatelé vytvoří nabídku na zastaralý případ požadavku na nabídku, zatímco probíhá jejich nabídka. Další informace o dodavatelské spolupráci naleznete v tématu [Dodavatelská spolupráce s externími dodavateli](vendor-collaboration-work-external-vendors.md). 

Pokud chcete pozvat další dodavatele k nabídce a nebyly provedeny žádné změny případu požadavku na nabídku, lze použít tlačítko **Odeslat**. Dodavatele, které jste přidali, se zobrazí na stránce **Odeslat** a dostanou pozvání e-mailem.

## <a name="receiving-and-registering-rfq-replies"></a>Příjem a registrace odpovědí na RFQ

Při odeslání požadavku na nabídku se automaticky vytvoří list odpovědi. Jakmile obdržíte odpovědi (nabídky) na požadavek na nabídku, zadejte informace od jednotlivých dodavatelů na list odpovědi na požadavek na nabídku pro jednotlivé dodavatele. Pokud přidáte kritéria hodnocení, můžete ohodnotit odpovědi. Nabídky dodavatelů můžete také porovnat pomocí hodnocení založeného na stanovených kritériích hodnocení, jako je například nejlepší celková cena nebo nejlepší celková doba dodání.

Pokud je dotazník připojen k případu požadavku na nabídku, je nutné ručně zadat odpovědi na otázky na listu odpovědí.

Můžete také přidat alternativní řádky, pokud případ požadavku na nabídku alternativní řádky umožňuje. Na pevné záložce **Řádky nákupní nabídky** vyberte **Přidat řádek**. Poté zadejte informace o produktu, například číslo položky nebo kategorii zásobování, množství, cenu a slevu.

Pokud jste zadali odpověď, ale požadujete novou nabídku od dodavatele, můžete znovu odeslat RFQ. Tím se vygeneruje nový deník a sestava, které můžete použít k vyžádání změn od dodavatele.

Přehled všech požadavků na nabídku a jejich stavy odpovědi naleznete na stránce **Zpracování požadavku na nabídku**.

Následující tabulka uvádí změny stavu požadavku na nabídku při příjmu nabídek a registraci informací na listu pro odpovědi na požadavek na nabídku.

| Akce                                         | Nejnižší stav nabídky | Nejvyšší stav nabídky | Nejnižší stav záhlaví požadavku na nabídku | Nejvyšší stav záhlaví požadavku na nabídku | Nejnižší stav řádky požadavku na nabídku | Nejvyšší stav řádky požadavku na nabídku |
|------------------------------------------------|-------------------|--------------------|--------------------------|---------------------------|------------------------|-------------------------|
| Zaregistrujte jednu nabídku od dodavatele a uložte ji.        | Odesláno              | Přijato           | Odesláno                     | Přijato                  | Odesláno                   | Přijato |
| Zaregistrujte druhou nabídku od dodavatele a uložte ji. | Přijato          | Přijato           | Přijato                 | Přijato                  | Přijato               | Přijato |

> [!NOTE]
> Pokud nabídku vrátíte dodavateli k dalšímu jednání, zůstane nejnižší i nejvyšší stav jako **Přijato**.

### <a name="accepting-and-rejecting-bids-and-transferring-accepted-bids-to-downstream-documents"></a>Přijetí a odmítnutí nabídek a přenos přijatých nabídek do podřízených dokumentů

Poté, co jste vybrali nejlepší nabídku, například nabídku, jež nabízí nejlepší celkovou cenu, nabídky přijměte. V nabídce můžete přijmout některé řádky a jiné zamítnout. Lze také přijímat řádky od různých dodavatelů. Počítejte s tím, že pokud přijmete některé řádky, budete vyzváni k odmítnutí všechny ostatních řádků. Z toho vyplývá, že pokud chcete přijmout další řádky, musíte zvolit **Zrušit** po zobrazení výzvy. Stav odpovědi na požadavek na nabídku pro každého dodavatele, od kterého přijímáte nabídky nebo řádky, je aktualizován na **Přijato**. 

Při přijetí nabídky nebo konkrétních řádků nabídky se automaticky vytvoří nákupní objednávka nebo nákupní smlouva. Poté můžete odmítnout nabídky od všech ostatních dodavatelů.

V odpovědi můžete přidat kód důvodu vysvětlující příčinu přijetí nebo odmítnutí nabídky.

Pokud přijmete odpověď RFQ s typem **Nákupní žádanka**, aktualizují řádky odpovědi RFQ řádky nákupní žádanky následujícími informacemi:

- Jednotková cena
- Procento slevy
- Částka slevy
- Doprovodné nákupní náklady
- Náklady pro řádek
- Dodavatel
- Externí hodnota
- Externí popis

Následující tabulka obsahuje změny stavu požadavku na nabídku při přijetí a odmítnutí nabídek od dodavatelů.

| Akce                      | Nejnižší stav nabídky | Nejvyšší stav nabídky | Nejnižší stav záhlaví požadavku na nabídku | Nejvyšší stav záhlaví požadavku na nabídku | Nejnižší stav řádky požadavku na nabídku | Nejvyšší stav řádky požadavku na nabídku |
|-------------------------    |-------------------|--------------------|--------------------------|---------------------------|------------------------|-------------------------|
| Přijměte jednu z nabídek.     | Přijato          | Akceptováno           | Přijato                 | Akceptováno                  | Přijato               | Akceptováno |
| Odmítněte všechny ostatní nabídky.  | Odmítnuto          | Akceptováno           | Odmítnuto                 | Akceptováno                  | Odmítnuto               | Přijato |

