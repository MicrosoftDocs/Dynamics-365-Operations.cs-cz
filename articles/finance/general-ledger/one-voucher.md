---
title: Jeden doklad
description: Jedno číslo dokladu pro finanční deníky (deník hlavní knihy, deník dlouhodobého majetku, deník platby dodavatele a tak dále) slouží k zadání více transakcí hlavní knihy v rámci jednoho dokladu.
author: kweekley
manager: AnnBe
ms.date: 11/05/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerParameters, AssetProposalDepreciation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 8.0.2
ms.openlocfilehash: 68ec3cb028462865e914cbcb25ff28dbaf9a4f01
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441212"
---
# <a name="one-voucher"></a>Jeden doklad

[!include [banner](../includes/banner.md)]


## <a name="what-is-one-voucher"></a>Co je Jeden doklad?

Existující funkce pro finanční deníky (deník hlavní knihy, deník dlouhodobého majetku, deník platby dodavatele a tak dále) slouží k zadání více transakcí dílčí hlavní knihy (odběratel, dodavatel, dlouhodobý majetek, projekt a banka) v kontextu jednoho dokladu. Microsoft nazývá tuto funkci jako *Jeden doklad*. Můžete vytvořit jediný doklad pomocí jedné z následujících metod:

- Nastavte název deníku (**Hlavní kniha** \> **Nastavení deníku** \> **Názvy deníků**) tak, aby pole **Nový doklad** bylo nastaveno na **Pouze číslo jednoho dokladu**. Všechny řádky, které přidáte do deníku, jsou nyní zahrnuty ve stejném dokladu. Proto lze doklad zadat jako doklad s více řádky, jako účet nebo protiúčet na stejném řádku nebo jako kombinaci.

    [![Jeden řádek](./media/same-line.png)](./media/same-line.png)

    > [!IMPORTANT]
    > Definice jednoho dokladu **nepokrývá** případy, kde jsou názvy deníků nastaveny jako **Pouze číslo jednoho dokladu**, ale uživatel poté zadá doklad, který obsahuje pouze typy účtů hlavní knihy. V tomto tématu 'Jeden doklad' znamená, že existuje jediný doklad, který obsahuje více než jednoho dodavatele, odběratele, banku, dlouhodobý majetek nebo projekt.

- Zadejte víceřádkový doklad, když neexistuje protiúčet.

    [![Víceřádkový doklad](./media/Multi-line.png)](./media/Multi-line.png)

- Zadejte doklad, kde účet i protiúčet obsahují typ účtu dílčí knihy, jako například **Dodavatel**/**Dodavatel**, **Odběratel**/**Odběratel**, **Dodavatel**/**Odběratel**, nebo **Banka**/**Banka**.

    [![Doklad dílčí hlavní knihy](./media/subledger.png)](./media/subledger.png)

## <a name="issues-with-one-voucher"></a>Potíže s jedním číslem dokladu

Funkce Jeden doklad způsobuje problémy při vyrovnání, výpočtu daně, stornu tranakce, odsouhlasení dílčí hlavní knihy do hlavní knihy, finančním výkaznictví atd. (Další informace o problémech, které mohou nastat během vyrovnání, získáte například v části [Jeden doklad s více záznamy odběratele nebo dodavatele](https://docs.microsoft.com/dynamics365/finance/accounts-payable/single-voucher-multiple-customer-vendor-records).) Správná práce a vykazování vyžaduje detaily transakce v těchto procesech a sestavách. Ačkoli některé scénáře mohou i nadále správně fungovat, v závislosti na nastavení vaší organizace dochází k častým problémům při zadávání více transakcí v jednom dokladu.

Předpokládejme například, že zaúčtujete následující víceřádkový doklad:

[![Příklad](./media/example.png)](./media/example.png)

Poté vygenerujete sestavu **Výdaje podle dodavatele** v pracovním prostoru **Finanční přehledy**. V této sestavě jsou zůstatky výdajových účtů seskupeny podle skupiny dodavatelů a poté dodavatele. Když je sestava vygenerována, systém nedokáže určit, kterým skupinám dodavatelů/dodavatelům vznikly výdaje 250,00. Vzhledem k tomu, že nebyly nalezeny podrobnosti o transakcích, systém bude předpokládat, že celé výdaje 250,00 jdou na vrub prvnímu dodavateli nalezenému v dokladu. Proto je výdaj 250,00, který je zahrnut do zůstatku na hlavním účtu 600120, uveden pod touto skupinou dodavatelů/dodavatelem. Je však velmi pravděpodobné, že první dodavatel v dokladu není správný dodavatel. Sestava je tedy pravděpodobně nesprávná.

[![Výdaj](./media/expenses.png)](./media/expenses.png)

## <a name="the-future-of-one-voucher"></a>Budoucnost funkce Jeden doklad

Z důvodu problémů, které byly zmíněny dříve, je funkce jednoho dokladu zastaralá. Protože však existují funkční mezery závislé na této funkci, funkce nezastarají všechny najednou. Místo toho se použije následující plán:

- **Verze Spring 2018** – Ve výchozím nastavení bude funkce vypnuta pomocí parametru **Povolit více transakcí v rámci jednoho dokladu** na kartě **Obecné** stránky **Parametry hlavní knihy**. Tuto funkci však můžete zapnout, pokud vaše organizace používá scénář, který spadá do jedné z funkčních mezer, které jsou uvedeny dále v tomto tématu.

    - Pokud mají zákazníci obchodní scénář, který nevyžaduje jeden doklad, neměli by zapínat tuto funkci. Microsoft nebude opravovat chyby v oblastech, které jsou identifikovány dále v tomto tématu, je-li tato funkce použita i v případě, že existuje jiné řešení.
    - Přestaňte používat Jeden doklad pro integrace, pokud funkcionalitu nepotřebujete pro jednu z funkčních mezer.

- **Nejnovější verze** – Všechny funkční mezery budou doplněny. **Po zaplnění funkčních mezer a doručení nových funkcí bude trvat ještě minimálně rok, než bude funkce jednoho dokladu trvale vypnuta**, protože zákazníci a nezávislí dodavatelé softwaru (ISV) musí mít dostatek času reagovat na novou funkci. Musí například aktualizovat své obchodní procesy, entity a integrace.

> [!IMPORTANT]
> Všimněte si, že možnost **pouze jedno číslo dokladu** **nebyla** odebrána z nastavení názvu deníku. Tato možnost je stále podporována, pokud doklad zahrnuje pouze typy účtů hlavní knihy. Odběratelé musí být opatrní, když toto nastavení používají, protože doklad se nezaúčtuje v případě, že používají **pouze jedno číslo dokladu**, ale poté zadají více než jednoho odběratele, dodavatele, banku, dlouhodobý majetek nebo projekt. Dále odběratelé také mohou zadat kombinaci typů účtů dílčí knihy, například platby v jednom dokladu, který obsahuje typy účtů **Dodavatel**/**Banka** .

## <a name="why-use-one-voucher"></a>Proč používat Jeden doklad?

Na základě rozhovorů s odběrateli společnost Microsoft zkompilovala následující seznam scénářů, kde odběratelé používají funkci jednoho dokladu nebo důvodů, proč ho používali. Některé z těchto obchodních požadavků lze splnit pouze pomocí jednoho dokladu. Však mnoho scénářích však alternativy mohou plnit stejné obchodní požadavky.

### <a name="scenarios-that-require-one-voucher"></a>Scénáře, které vyžadují jeden doklad

Následujících scénářů lze dosáhnout pouze pomocí funkce jednoho dokladu. Pokud vaše organizace má některý z uvedených scénářů, je nutné povolit více transakcí, které mají být zadány do dokladu změnou nastavení parametru **Povolit více transakcí v rámci jednoho dokladu** na stránce **Parametry hlavní knihy**. Tyto funkční mezery budou vyplněny pomocí dalších funkcí v novějších verzích.

> [!Note]
> [Pro každý z následujících scénářů musí být pole **Povolit více transakcí v rámci jednoho dokladu** musí být nastaveno na Ano na pevné záložce **Obecné** na stránce **Parametry hlavní knihy**.]

### <a name="post-vendor-or-customer-payments-in-summary-form-to-a-bank-account"></a>Zaúčtování plateb dodavatelů v souhrnné formě na bankovní účet

**Scénář** Organizace komunikuje seznam dodavatelů a částky do jeho banky a banka používá tento seznam pro platby dodavatelů jménem organizace. Banka zaúčtuje součet plateb jako jeden výběr na bankovním účtu.

Souhrnu plateb dodavatele je podporován pouze prostřednictvím jednoho dokladu. Každý dodavatel je zadán jako samostatný řádek pro udržování podrobností v dílčí hlavní knize závazků. Souhrnná částka všech plateb je však posunuta na jediný řádek pro bankovní účet. Zrušení se tedy zobrazí jako jedna souhrnná částka v dílčí knize banky.

**Scénář** Organizace vkládá platby odběratele nebo bankovní vklady plateb odběratele jménem organizace jako paušální částku a na bankovním účtu se zobrazí záloha po uložení.

Souhrn plateb odběratele je obvykle podporován prostřednictvím funkce vkladu. Pokud ale používáte "překlenovací" metody platby, v tomto scénáři jsou podporovány pouze v rámci jednoho dokladu. Stejným způsobem, popsaným pro souhrn plateb dodavatele, se zadávají platby odběratele.

### <a name="mechanism-to-group-transactions-from-a-business-event"></a>Mechanismus k seskupení transakcí z obchodní události

**Scénář** Organizace má jednu obchodní událost, která spouští několik transakcí. Účetní oddělení však chce zobrazit účetní položky společně, aby bylo možné lépe provádět audit.

Pokud organizace musí zobrazit účetní položky z obchodní události společně, musí používat jedno číslo dokladu. 

### <a name="country-specific-features"></a>Funkce specifické pro zemi

**Scénář** Funkce jednoho správního dokumentu (SAD) pro Polsko aktuálně vyžaduje použití jednoho dokladu. Dokud nebude pro tuto funkci možnost seskupení k dispozici , je nutné nadále používat funkci jednoho dokladu. Mohou existovat další funkce specifické pro zemi, které vyžadují funkci jednoho dokladu.

### <a name="customer-prepayment-payment-journal-that-has-taxes-on-multiple-lines"></a>Zálohový doklad deníku zákazníka, který má daně na více řádcích

V tomto případě je zákazník na jednom dokladu stejný vzhledem k tomu, že transakce simuluje řádky objednávky odběratele. Je nutné zadat zálohu do jednoho dokladu, protože výpočet daně musí být proveden na řádcích jedné platby provedené odběratelem.

### <a name="customer-reimbursement"></a>Refundace zákazníka

**Scénář** Odběratel provede zálohu pro objednávku a řádky objednávky mají jiné daně, které musí být zaznamenány pro zálohu. Zálohová platba odběratele je jedna transakce simulující řádky objednávky, aby bylo možné zaznamenat příslušnou daň pro částku na každém řádku.

Pokud je periodická úloha refundace spuštěna z modulu pohledávek, vytváří transakci pro přesun zůstatku od zákazníka k dodavateli. V tomto scénáři musí být použit jeden doklad pro refundaci zákazníka.

### <a name="fixed-asset-maintenance-catch-up-depreciation-split-asset-calculate-depreciation-on-disposal"></a>Údržba dlouhodobého majetku: opravný odpis, rozdělení majetku, výpočet odpisu pro vyřazení
Následujících transakce dlouhodobého majetku také vytvoří více transakcí v jedno dokladu:

- Je provedeno další pořízení dlouhodobého majetku a je vypočten 'opravný' odpis.
- Majetek je rozdělen.
- Je zapnutý parametr k vypočtení odpisu pro vyřazení, a pak je majetek vyřazen.
- Datum uvedení majetku do služby je před datem pořízení. Z tohoto důvodu je zaúčtována oprava odpisu.

> [!Note]
> Při zadávání transakcí zkontrolujte, zda se všechny transakce vztahují ke stejnému dlouhodobému majetku. Doklad nebude zaúčtován, pokud zahrnuje více než jeden dlouhodobý majetek, a to i v případě, že je pole **Nový doklad** nastaveno na jedno číslo dokladu pouze na stránce **Názvy deníku** v hlavní knize. Pokud do dokladu zahrnete více než jeden dlouhodobý majetek, může se zobrazit zpráva **Na doklad může existovat jen jedna transakce dlouhodobého majetku** a tento doklad nebude možné zaúčtovat.  

### <a name="bills-of-exchange-and-promissory-notes"></a> Cizí směnky a vlastní směnky
Cizí směnky a vlastní směnky vyžadují, aby byl použit jeden doklad, protože transakce přesouvají zůstatek zákazníka nebo dodavatele z jednoho účtu hlavní knihy pohledávek/závazků na jiný, na základě stavu platby.

## <a name="scenarios-that-dont-require-one-voucher"></a>Scénáře, které nevyžadují jeden doklad

Následujících scénářů lze dosáhnout pomocí jiných prostředků a neměly by používat funkci jednoho dokladu.

### <a name="post-customer-payments-in-summary-form-to-the-bank-account"></a>Zaúčtování plateb odběratelů v souhrnné formě na bankovní účet

Organizace vkládá platby odběratele nebo bankovní vklady plateb odběratele jménem organizace jako paušální částku a na bankovním účtu se zobrazí záloha po uložení.

Souhrn plateb odběratele je podporován prostřednictvím funkce vkladou, když se u metody platby nepoužívá překlenování.

### <a name="netting"></a>Určování čistých částek

V započtení jsou zůstatky dodavatelů a odběratelů vyrovnány s prodejními objednávkami vzájemně vzhledem k tomu, že dodavatel a odběratel představují stejnou stranu. Tento přístup minimalizuje výměnu peněz mezi organizací a stranou odběratele/dodavatele.

Započtení lze provést zadáním zvýšení a snížení v samostatných dokladech a zaúčtování protiúčtu pro zúčtovací účet hlavní knihy.

### <a name="post-in-summary-to-the-general-ledger"></a>Zaúčtování souhrnu do hlavní knihy

Organizace často chtějí účtovat do hlavní knihy souhrnně, aby se minimalizovalo množství dat. Organizace však ještě obvykle vyžadují zachování podrobností transakce. Po zaúčtování v souhrnu pomocí jednoho dokladu nejsou známy detaily transakce a nelze je spravovat.

- Vzhledem k tomu, že detaily transakce aktuálně nelze spravovat, doporučujeme organizacím **nepoužívat** jeden doklad pro zaúčtování v souhrnné formě.
- Po odstranění podpory jednoho dokladu lze implementovat architekturu zdrojového dokumentu a účtování do deníků. Tyto architektury budou poté spravovat podrobnosti transakce a podporovat souhrny do hlavní knihy.


### <a name="settle-multiple-unposted-payments-to-the-same-invoice"></a>Vyrovnání více nezaúčtovaných plateb na stejné faktuře

K tomuto scénáři obvykle dochází v organizacích, kde mohou odběratelé použít několik metod platby pro zaplacení nákupů. V tomto scénáři musí být organizace schopná zaznamenat více nezaúčtovaných plateb a vyrovnat je proti faktuře odběratele.

Nové funkce, které byly přidány do aplikace Microsoft Dynamics 365 for Operations verze 1611 (listopad 2016) umožňují vypořádat více nezaúčtovaných plateb do vyrovnány u jedné faktury. Vícenásobné platby odběratele se již nezadávají v jednom dokladu.

### <a name="import-bank-statement-transactions"></a>Import transakcí bankovního výpisu

Banky často platí a přijímají platby v zastoupení organizace, a tyto transakce se zaznamenávají v modulu Finance prostřednictvím souboru přijatého od banky. Organizace často chtějí seskupit tyto transakce pomocí čísla bankovního výpisu v souboru. Vzhledem k tomu, že každá transakce je zobrazena podrobně na bankovním výpisu, není požadována žádná sumarizace v dílčí knize banky.

Transakce mohou být seskupeny pomocí dalších polí v deníku, jako je například samotné číslo dávky deníku nebo číslo dokumentu.


### <a name="transfer-balances"></a>Převod zůstatků

Může být potřeba, aby organizace převedla zůstatek z jednoho dodavatele na jiného dodavatele, buď protože došlo k chybě, nebo proto, že jiný dodavatel převzal zodpovědnost. Převody tohoto typu se také dějí pro typy účtu, jako jsou **Zákazník** a **Banka**.

Převody zůstatků z jednoho účtu (dodavatele, odběratele, banky a tak dále) na jiný účet a protiúčet lze provádět prostřednictvím samostatných dokladů, a vyrovnání lze zaúčtovat na zúčtovací účet hlavní knihy.

### <a name="enter-beginning-balances"></a>Zadání počátečních zůstatků

Organizace často zadávají počáteční zůstatky pro účty vedlejší knihy (dodavatelé, odběratelé, dlouhodobého majetku atd.) jako transakce s jedním číslem dokladu. Počáteční zůstatky pro každý účet vedlejší knihy lze zadat jako samostatné doklady a zaúčtovat rozdíl na zúčtovací účet hlavní knihy.

### <a name="correct-the-accounting-entry-of-a-posted-customer-or-vendor-document"></a>Opravit účetní položky zaúčtovaného dokladu odběratele nebo dodavatele

Může být nutné, aby organizace opravila účet závazků nebo pohledávek v hlavní knize pro účtování položky zaúčtované faktury, ale tuto fakturu nelze stornovat nebo opravit pomocí jiného mechanismu.

Je-li nutné u pohledávek pro vybrané účty hlavní knihy splatných účtů provést opravu, je nutné provést úpravy přímo do účtu hlavní knihy. Úpravu nelze provést pomocí zaúčtování prostřednictvím odběratele nebo dodavatele. Tento přístup vyžaduje, aby byly provedeny úpravy během prostoje, aby účet hlavní knihy dočasně umožňoval ruční zadávání.

### <a name="the-system-allows-it"></a>Systém to umožňuje"

Organizace často používají funkci jednoho dokladu pouze proto, že jim systém umožňuje používat je bez pochopení důsledků.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]