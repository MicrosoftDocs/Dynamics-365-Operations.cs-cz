---
title: "Požadavek na nabídky (RFQ)"
description: "Toto téma poskytuje přehled požadavků na nabídku (RFQs), které organizace vydávají v případě, že musí nakoupit položky nebo služby a chtějí získat od několika dodavatelů konkurenční nabídky."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchRFQCaseTable, PurchRFQCaseTableListPage, PurchRFQCompare, PurchRFQReplyTable, PurchRFQVendReplyTableListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2154
ms.assetid: 3936996e-d943-46ca-8385-84c042990f1d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8b817ffd905f1d3e99befc149416006e1a51f5e2
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="request-for-quotations-rfqs"></a>Požadavek na nabídky (RFQ)

[!include[banner](../includes/banner.md)]


Toto téma poskytuje přehled požadavků na nabídku (RFQs), které organizace vydávají v případě, že musí nakoupit položky nebo služby a chtějí získat od několika dodavatelů konkurenční nabídky. V požadavku na nabídku požádejte dodavatele o zadání cen a dodacích lhůt pro zadané množství položek. Lze také požádat dodavatele, aby určili, zda budou účtovány vedlejší náklady, například přepravní náklady nebo slevy pro velké objednávky či včasnou platbu za fakturu dodavatele.

Požadavek na nabídku (RFQ) zahrnuje následující úkoly:

-   vytvoření a odeslání požadavku na nabídku jednomu nebo více dodavatelům,
-   příjem a registraci odpovědí na RFQ (nabídek),
-   Převod přijatých nabídek na nákupní objednávky, nákupní smlouvu nebo nákupní žádanku.

Následující obrázek přehledně znázorňuje průběh zpracování požadavku na nabídku.  

[![Proces požadavku na nabídku](./media/rfq-process-458x1024.jpg)](./media/rfq-process.jpg)  

Požadavek na nabídku můžete vytvořit z plánovaných objednávek z nákupní žádanky a z ručního zadání. Požadavek na nabídku, který vytvoříte, se nazývá případ požadavku na nabídku a je základní dokument, který použijete k vystavení nabídky pro každého dodavatele. Po přípravě případu RFQ a přidání dodavatelů klikněte na tlačítko **Odeslat** v případu požadavku na nabídku a pro každého dodavatele, kterému jste odeslali RFQ , se vytvoří deník RFQ. Můžete nakonfigurovat nastavení správy tisku pro akci Odeslat vytisknout sestavu pro každého dodavatele do archivu nebo odeslat sestavu na e-mailovou adresu každého dodavatele. Deník požadavku na nabídku pro každého dodavatele lze navíc použít k vytvoření sestavy, kterou lze odeslat nebo později znovu odeslat dodavateli. Také můžete nakonfigurovat akce Odeslání a vygenerovat list odpovědí, který mohou vyplňovat dodavatelé.  

Pokud se po odeslání musí požadavek na nabídku změnit, můžete opětně odeslat požadavek na nabídku dodavatelům po dokončení úprav.  

Jakmile obdržíte nabídky, je nutné je zadat na stránce **Odpovědi na požadavky na nabídku**. Pokud jste vybrali možnost **Kopírovat data do odpovědi**, data jako například množství a data z případu požadavku na nabídku jsou zkopírovány do odpovědi na nabídku. Tato data lze změnit podle nabídky dodavatele.  

Pokud je druhá iterace odpovědi vyžadována pro určitého dodavatele, klepněte na tlačítko **Vrácení** na stránce **Odpověď požadavku na nabídku**. Akce Vrácení vytvoří nový deník a sestavu, která bude vytištěna, archivována a odeslána podle nastavení správy tisku.  

Pokud jste přidali kritéria hodnocení do případu požadavku na nabídku, odpověď požadavku na nabídku bude mít panel hodnocení, kde můžete zadat výsledky. Celkové hodnocení se zobrazí při porovnání odpovědí na stránce **Porovnat odpovědi**, kde můžete také porovnat jiná data odpovědi, jako například ceny řádku, datum dodání a celkovou cenu.  

Po rozhodnutí, zda chcete použít nabídku nebo dílčí nabídku, můžete je přijmout a odmítnout ostatní. Jsou generovány deníky přijetí, deníky odmítnutí a příslušné sestavy. Tyto budou vytištěny, archivovány a odeslány podle nastavení správy tisku. Při přijetí nabídky nebo konkrétních řádků v nabídce bude vytvořena nákupní smlouva nebo nákupní objednávka nebo aktualizován nákupní požadavek – v závislosti na typu nákupního požadavku na nabídku. Můžete vytvořit obchodní smlouvu, kterou můžete později použít u všech odpovědí, bez ohledu na to, zda jste je přijali nebo zamítli.  

Stav požadavku na nabídku se zobrazí v záhlaví požadavku na nabídku a závisí na stavu řádků požadavku na nabídku. Stav označuje rozsah, do kterého byl zpracován požadavek na cenovou nabídku. Každý požadavek na nabídku má dvě hodnoty stavu: nejnižší a nejvyšší. Nejnižší stav je nejméně pokročilou fází jakékoli řádky v požadavku na nabídku a nejvyšší stav je nejpokročilejší fází jakékoli řádky v požadavku na nabídku. Pokud je například poslední pokročilá fáze v požadavku na nabídku určena pro řádku, která byla vytvořena, bude nejnižší fáze požadavku **Vytvořeno**. Pokud je nejpokročilejší fáze v požadavku na nabídku určena pro řádku, která byla odeslána dodavatelům, bude její nejvyšší stav **Odesláno**. Stavy jsou automaticky aktualizovány při zpracování požadavku na nabídku.  

Nejnižší a nejvyšší stav záhlaví požadavku na nabídku můžete zobrazit na stránce **Všechny požadavky na nabídky**. Nejnižší a nejvyšší stav řádku požadavku na nabídku můžete zobrazit na kartě **Řádky** na stránce **Požadavky na nabídky**.  

Pořadí stavů zpracování požadavku na nabídku vypadá takto:

1.  **Vytvořeno**
2.  **Odesláno**
3.  **Přijato**
4.  **Přijato**/**Zrušeno**/**Odmítnuto**

Stavy budou popsány podrobněji pozdější v tomto tématu.

## <a name="setting-up-rfq-functionality"></a>Nastavení funkce RFQ
Než bude možné vytvořit případ požadavku na nabídku, je nutné konfigurovat informace o požadavku na nabídku na stránce **Parametry modulu Zásobování a zdroje**. Při vytváření případu požadavku na nabídku lze zadat výchozí hodnoty, které budou zkopírovány do požadavku na nabídku. Můžete zadat následující výchozí hodnoty:

-   Typ nákupu nového požadavku na nabídku: **Nákupní objednávka** nebo **Nákupní smlouva**.
-   Nastavení data a času vypršení platnosti.
-   Informace o dodání a platební podmínky.
-   Pole, která mají být zahrnuta v odpovědi na požadavek na nabídku.

Tyto hodnoty lze přepsat pro konkrétní případ požadavku na nabídku. Také je třeba nakonfigurovat proces změn. V rámci této konfigurace můžete zapnout blokování pole. Pokud je zapnuto uzamčení pole, musí zásobovací pracovník, který chce změnit RFQ, nejprve kliknout na **Vytvořit** v části **Dodatek** na záložce **Nabídka**. Poté, co byla RFQ aktualizována dodatkem, musí zásobovací pracovník dokončit proces kliknutím na **Dokončit**. Akce **Finalizovat** vytvoří e-mailovou zprávu, která upozorní dodavatele na doplněnou RFQ. Vyberte šablonu pro oznámení e-mailem odeslané dodavatelům na stránce **Parametry modulu Zásobování a zdroje**. Po vytvoření šablona může obsahovat následující náhradní tokeny:

-   %Důvod pro vrácení nabídky%
-   %Důvod pro dodatek%
-   %Pořizovatel dodatku%
-   %Společnost%

Tokeny %Důvod pro vrácení nabídky% a %Důvod pro dodatek% jsou nahrazeny textem, který pracovník zásobování může zadat po dokončení dodatku v průvodci **Dodatek**. Hodnoty pro token %Pořizovatel dodatku% a %Společnost% jsou automaticky převzaty z požadavku na nabídku.  

Pokud chcete použít kódy důvodu u odpovědi na požadavek na nabídku a označit tak, proč nabídka byla zamítnuta nebo přijata, musíte nastavit kódy důvodu na stránce **Dodavatel – důvody**.  

Vzhled vytištěných a uložených dokumentů požadavku na nabídku můžete nakonfigurovat na stránce **Nastavení formuláře** v modulu Zásobování a zdroje. 

**Poznámka:** U konfigurace veřejného sektoru platí, že jakékoli změny provedené v RFQ, která již byla odeslána, budou vyžadovat použití procesu dodatku. Při odeslání požadavku na nabídku jsou pole uzamčena, takže klepnutí na **Vytvořit** pro použití procesu dodatku, jak je popsáno výše, je povinný krok k provedení změn požadavku.
To určuje parametr uzamčení pole **Zamknout požadavky na nabídku při odeslání** v poli **Parametry modulu zásobování a zdroje**. Tento parametr je nastaven na **Ano** a pro konfiguraci veřejného sektoru se jedná o výchozí hodnotu, kterou nelze změnit. To znamená, že zatímco proces dodatku lze zpracovat ručně v konfiguraci neveřejného sektoru, proces zpracování dodatků uzamčením polí po odeslání požadavku na nabídku je povinný pro veřejný sektor.

Při vytváření požadavku na nabídku pro nákupní objednávku a přidávání skladových položek do požadavku na nabídku bude vytvořena také skladová transakce, která má stav příjmu **Příjem nabídky**. Při výpočtu zásob pomocí hlavního plánu jsou použity pouze řádky požadavku na nabídku tohoto stavu. Pokud chcete, aby hlavní plán zahrnoval řádky požadavku na nabídku jako očekávaný příjem, je nutné konfigurovat toto chování v nastavení hlavního plánování.  

Jako správce nebo zástupce nákupu můžete vytvořit a spravovat typy oslovení, aby splňovaly požadavky zásobování pro vaši organizaci. Každý typ oslovení může řídit metody hodnocení. Metody hodnocení obsahují sadu kritérií, kterou lze použít, pokud dosáhnete úspěšné nabídky. Je nutné nastavit typy oslovení, metody hodnocení a kritéria hodnocení na stránce **Typ oslovení** a **Metoda hodnocení**.

## <a name="creating-and-sending-an-rfq"></a>Vytvoření a odeslání požadavku na nabídku
Vytvořte požadavek na nabídku, vyberte dodavatele, který má zadat nabídku k požadavku na nabídku a odešlete požadavek na nabídku dodavatelům. Správu tisku můžete použít pro směrování sestavy požadavku na nabídku a listu odpovědí do upřednostňovaného cíle.  

Můžete vytvořit požadavku na nabídku pro typ nákupu **Nákupní objednávka** nebo **Nákupní smlouva**.  

Je-li požadavek na nabídku generován na základě nákupního požadavku, typ **Nákupní žádanka** je automaticky přiřazen. Nelze vytvořit ručně požadavek na nabídku typu **Nákupní žádanka**. Pokud je požadavek na nabídku typu **Nákupní objednávka**:

-   Při vytvoření řádků požadavku na nabídku se vytvoří skladové transakce, které mají stav příjmu **Příjem nabídky**.
-   Při přijetí nabídky je vygenerována nákupní objednávka.

Pokud je požadavek na nabídku typu **Nákupní smlouva**:

-   Požadavek na nabídku se používá pro dohodu o nákupu určitého množství nebo hodnoty produktu během času. Musíte vybrat rozsah dat, který se týká nákupní smlouvy a jména osoby, která spravuje nákupní smlouvu.
-   Při přijetí nabídky je vygenerována nákupní smlouva.

Požadavek na nabídku z nákupního požadavku můžete vytvořit pouze v případě, že je stav nákupního požadavku **Probíhá kontrola** a je vám přiřazeno provádět další úlohy workflowu. Řádky nákupního požadavku se automaticky aktualizují, jakmile přijmete řádky z odpovědí na požadavky na nabídku (nabídky), které jste získali od dodavatelů. Pokud probíhá zpracování RFQ, nelze provést žádné akce nákupní žádanky (například dokončení, odmítnutí nebo schválení).  

Pokud vytvoříte požadavek na nabídku, můžete vybrat konkrétní typ oslovení. Typ oslovení určuje sadu kritérií hodnocení, která se používá k získání odpovědí na požadavky na nabídku.  

K případu požadavku na nabídku můžete přiřadit dotazník. Tento dotazník se objeví na všech odpovědích po odeslání požadavku na nabídku.  

Máte na výběr tři způsoby, jak vybrat dodavatele a přidat jej k případu požadavku na nabídku:

-   Přidání dodavatelů po jednom.
-   Vyhledání všech dodavatelů, které splňují konkrétní kritéria.
-   Automatické přidání všech dodavatelů, kteří byli schváleni pro kategorie zásobování, které se používají v řádcích požadavku na nabídku.

Jakmile je případ požadavku na nabídku připraven, klepněte na tlačítko **Odeslat**. Akce Odeslat vytvoří deník a sestavy, které budou vytištěny, archivovány a odeslány podle nastavení správy tisku.  

Pokud jste označili pole **Použít dodavatele pro přepočítávání cen** a **Použít informace o položce specifické pro prodejce** na stránce **Odesílání požadavku na nabídku**, když jste odeslali požadavek dodavatelům, některé informace pro konkrétní dodavatele budou automaticky doplněny. Tyto informace můžete upravit na stránce **Odpověď požadavku na nabídku**.  

Následující tabulka uvádí změny stavu požadavku na nabídku při vytvoření nabídky a jejím odeslání dodavatelům.

|                                    |                              |                                                 |                            |                             |
|------------------------------------|------------------------------|-------------------------------------------------|----------------------------|-----------------------------|
| **Akce**                         | **Nejnižší stav záhlaví požadavku na nabídku** | **Nejvyšší stav záhlaví požadavku na nabídku**                   | **Nejnižší stav řádky požadavku na nabídku** | **Nejvyšší stav řádky požadavku na nabídku** |
| Vytvoření záhlaví RFQ a řádku.    | Vytvořeno                      | Vytvořeno                                         | Vytvořeno                    | Vytvořeno                     |
| Odešlete požadavek na cenovou nabídku konkrétního dodavatele. | Odesláno                         | Odesláno                                            | Odesláno                       | Odesláno                        |
| Přidejte jiného dodavatele.                | Vytvořeno                      | Odešlete (požadavek na nabídku byl zaslán pouze jednomu dodavateli.) | Vytvořeno                    | Odesláno                        |
| Odešlete požadavek na nabídku druhému dodavateli. | Odesláno                         | Odesláno                                            | Odesláno                       | Odesláno                        |

**Poznámka:** Do požadavku na nabídku můžete kdykoli přidat další dodavatele a nejnižší a nejvyšší stav se změní podle nových dodavatelů. Pokud jste například přijali nabídky od všech dodavatelů a přijali alespoň jeden řádek v nabídce, bude nejnižší stav v hlavičce požadavku na nabídku **Odmítnuto** a nejvyšší stav **Přijato**. Pokud přidáte nového dodavatele, bude nejnižší stav v jakémkoli řádku **Vytvořeno**. Nejnižší stav v záhlaví požadavku na nabídku se tedy změní na **Vytvořeno** a nejvyšší zůstane **Přijato**.

## <a name="amending-an-rfq"></a>Změna požadavku na nabídku
V některých případech je nutné požadavek na nabídku změnit po odeslání. To může nastat například v případě, kdy byla změněna data dodání, nebo když požadujete další výrobky nebo jiné množství produktů. Proces dodatku můžete nakonfigurovat tak, aby bylo omezení větší nebo menší.  

Používáte-li proces většího omezení, musíte před změnou polí v případu požadavku na nabídku klepnout na **Vytvořit** u případu požadavku na nabídku a spustit tak změnu. Po dokončení změn je nutné klepnout na **Dokončit**. Poté bude provedeni procesem přidání informací pro e-mailovou zprávu, která bude odeslána pro upozornění dodavatelů na změnu. Aktualizovaná sestavy požadavku na nabídku, která zahrnuje poznámku o změně, je automaticky přiřazena ke zprávě.  

Používáte-li proces menšího omezení, nemusíte vytvořit změnu předtím, než bude možné upravit pole v případu požadavku na nabídku, který již byl odeslán. Musíte však ručně přidat poznámku o změně do požadavku na nabídku.

## <a name="receiving-and-registering-rfq-replies"></a>Příjem a registrace odpovědí na RFQ
Při odeslání požadavku na nabídku se automaticky vytvoří list odpovědi. Jakmile obdržíte odpovědi (nabídky) na požadavek na nabídku, zadejte informace od jednotlivých dodavatelů na list odpovědi na požadavek na nabídku pro jednotlivé dodavatele. Pokud přidáte kritéria hodnocení, můžete ohodnotit odpovědi. Nabídky dodavatelů můžete také porovnat pomocí hodnocení založeného na stanovených kritériích hodnocení, jako je například nejlepší celková cena nebo nejlepší celková doba dodání.  

Pokud je dotazník připojen k případu požadavku na nabídku, je nutné ručně zadat odpovědi na otázky do listu odpovědí.  

Pokud je nutné zadat alternativní řádky, a případ požadavku na nabídku to umožňuje, na pevné záložce **Řádky nákupní nabídky** klepněte na tlačítko **Přidat řádek**. Poté zadejte informace o produktu, například číslo položky nebo kategorii zásobování, množství, cenu a slevu.  

Pokud jste zadali odpověď, ale požadujete novou nabídku od dodavatele, můžete znovu odeslat RFQ. Tím se vygeneruje nový deník a sestava, které můžete použít k vyžádání změn od dodavatele.  

Přehled všech požadavků na nabídku a jejich stavy odpovědi naleznete na stránce **Zpracování požadavku na nabídku**.  

Následující tabulka uvádí změny stavu požadavku na nabídku při příjmu nabídek a registraci informací v listu pro odpovědi na požadavek na nabídku.

|                                                |                       |                        |                              |                               |                            |                             |
|------------------------------------------------|-----------------------|------------------------|------------------------------|-------------------------------|----------------------------|-----------------------------|
| **Akce**                                     | **Nejnižší stav nabídky** | **Nejvyšší stav nabídky** | **Nejnižší stav záhlaví požadavku na nabídku** | **Nejvyšší stav záhlaví požadavku na nabídku** | **Nejnižší stav řádky požadavku na nabídku** | **Nejvyšší stav řádky požadavku na nabídku** |
| Zaregistrujte první nabídku od dodavatele a uložte ji.        | Odesláno                  | Přijato               | Odesláno                         | Přijato                      | Odesláno                       | Přijato                    |
| Zaregistrujte druhou nabídku od dodavatele a uložte ji. | Přijato              | Přijato               | Přijato                     | Přijato                      | Přijato                   | Přijato                    |

**Poznámka:** Pokud nabídku vrátíte dodavateli k dalšímu jednání, zůstane nejnižší i nejvyšší stav **Přijato**.

### <a name="accepting-and-rejecting-bids-and-transferring-accepted-bids-to-downstream-documents"></a>Přijetí a odmítnutí nabídek a přenos přijatých nabídek do podřízených dokumentů

Poté, co jste vybrali nejlepší nabídku, například nabídku, jež nabízí nejlepší celkovou cenu, nabídky přijměte. Stav odpovědi na požadavek nabídku dodavatele je aktualizován na **Přijato**. Při přijetí nabídky nebo konkrétních řádků nabídky se automaticky vytvoří nákupní objednávka nebo nákupní smlouva, a vy získáte možnost odmítnout nabídky od ostatních dodavatelů.  

Pokud přijmete odpověď RFQ s typem **Nákupní žádanka**, aktualizují řádky odpovědi RFQ řádky nákupní žádanky následujícími informacemi:

-   Jednotková cena
-   Procento slevy
-   Částka slevy
-   Doprovodné nákupní náklady
-   Náklady pro řádek
-   Dodavatel
-   Externí hodnota
-   Externí popis

V odpovědi můžete přidat kód důvodu vysvětlující příčinu přijetí nebo odmítnutí nabídky.  

V nabídce můžete přijmout některé řádky a jiné zamítnout. Lze také přijímat řádky od různých dodavatelů. Počítejte s tím, že pokud přijmete některé řádky, budete vyzváni k odmítnutí všechny ostatních řádků. Z toho vyplývá, že pokud chcete přijmout další řádky, musíte klepnout na **Zrušit** po zobrazení výzvy.  

Následující tabulka obsahuje změny stavu požadavku na nabídku při přijetí a odmítnutí nabídek od dodavatelů.

|                         |                       |                        |                              |                               |                            |                             |
|-------------------------|-----------------------|------------------------|------------------------------|-------------------------------|----------------------------|-----------------------------|
| **Akce**              | **Nejnižší stav nabídky** | **Nejvyšší stav nabídky** | **Nejnižší stav záhlaví požadavku na nabídku** | **Nejvyšší stav záhlaví požadavku na nabídku** | **Nejnižší stav řádky požadavku na nabídku** | **Nejvyšší stav řádky požadavku na nabídku** |
| Přijměte jednu z nabídek. | Přijato              | Přijato               | Přijato                     | Přijato                      | Přijato                   | Přijato                    |
| Odmítněte ostatní nabídky.  | Odmítnuto              | Přijato               | Odmítnuto                     | Přijato                      | Odmítnuto                   | Přijato                    |






