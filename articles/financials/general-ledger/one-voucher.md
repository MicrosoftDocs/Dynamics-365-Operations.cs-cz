---
title: Jeden doklad
description: "Jedno číslo dokladu pro finanční deníky (deník hlavní knihy, deník dlouhodobého majetku, deník platby dodavatele a tak dále) slouží k zadání více transakcí hlavní knihy v rámci jednoho dokladu."
author: kweekley
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 9f996131830f9bd4efd534143b3fb761c5ccc756
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---

# <a name="one-voucher"></a>Jeden doklad

[!INCLUDE [banner](../includes/banner.md)]

> [!NOTE]
>  Tato funkce bude k dispozici v aplikaci Dynamics 365 for Finance and Operations verze 8.0, která bude k dispozici ve vydání Spring '18.   

<a name="what-is-one-voucher"></a>Co je Jeden doklad?
======================

Existující funkce pro finanční deníky (deník hlavní knihy, deník dlouhodobého majetku, deník platby dodavatele a tak dále) slouží k zadání více transakcí hlavní knihy v rámci jednoho dokladu. Tuto funkci označujeme jako Jeden doklad. Můžete vytvořit Jeden doklad pomocí jedné z následujících metod:

-   Nastavte název deníku (**Hlavní kniha** \> **Nastavení deníku** \>**Názvy deníků**) tak, aby pole **Nový doklad** bylo nastaveno na **Pouze jedno číslo dokladu**. * Všechny řádky, které přidáte do deníku, jsou nyní zahrnuty na stejném dokladu. Vzhledem k tomu, že je každý řádek přidán do jednoho dokladu, doklad lze zadat pro více řádků dokladu, jako účet nebo protiúčet na stejném řádku nebo kombinaci.

[![Jeden řádek](./media/same-line.png)](./media/same-line.png)
 
> [!IMPORTANT] 
> *  Nezapomeňte, že definice jednoho dokladu neobsahuje názvy deníků, které jsou nastaveny pouze jako **jedno číslo dokladu** a uživatel poté zadá doklad, který obsahuje pouze typy účtů hlavní knihy.  V tomto dokumentu 'Jeden doklad' znamená, že existuje jeden doklad, který obsahuje více než jednoho dodavatele, odběratele, banku, dlouhodobý majetek nebo projekt. 

-   Zadejte víceřádkový doklad, když neexistuje protiúčet.

[![Víceřádkový doklad](./media/Multi-line.png)](./media/Multi-line.png)

-   Zadejte doklad, kde účet i protiúčet obsahují typ účtu dílčí knihy, jako například typ účtu, dodavatel/dodavatel, odběratel/odběratel, dodavatele/odběratel nebo banka/banka.

[![Doklad dílčí hlavní knihy](./media/subledger.png)](./media/subledger.png)

<a name="issues-with-one-voucher"></a>Potíže s jedním číslem dokladu
=======================

Funkce Jeden doklad způsobuje problémy při vyrovnání, výpočtu daně, odsouhlasení dílčí hlavní knihy do hlavní knihy, finančním výkaznictví atd. (Další informace o problémech, které mohou nastat během vyrovnání, získáte v části [Jeden doklad s více záznamy odběratele nebo dodavatele](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/accounts-payable/single-voucher-multiple-customer-vendor-records).) Správná práce a vykazování vyžaduje detaily transakce v těchto procesech a sestavách. Ačkoli některé scénáře mohou i nadále správně fungovat, na základě nastavení vaší organizace dochází k častým problémům při zadávání více transakcí v jednom dokladu.

Předpokládejme například, že zaúčtujete následující víceřádkový doklad:

[![Příklad](./media/example.png)](./media/example.png)

Poté vygenerujete sestavu **Výdaje podle dodavatele** v pracovním prostoru **Finanční přehledy**. Sestava seskupuje zůstatky výdajových účtů pod skupinou dodavatelů a dodavatelem. Při generování sestavy systém nedokáže určit, kterým skupinám dodavatelů/dodavatelům vznikly výdaje 250,00. Vzhledem k tomu, že nebyly nalezeny podrobnosti o transakcích, systém bude předpokládat, že celá hodnota 250,00 vznikla nalezením prvního dodavatele v dokladu. Částka 250,00, která je zahrnuta do zůstatku na hlavním účtu 600120, je pak uvedena pod touto skupinou dodavatelů/dodavatelem. Je velmi pravděpodobné, že první dodavatel v dokladu nebyl správný dodavatel, takže sestava je nesprávná.

[![Výdaj](./media/expenses.png)](./media/expenses.png)

<a name="the-future-of-one-voucher"></a>Budoucnost funkce Jeden doklad
=========================

Z důvodu problémů, které byly uvedeny dříve, je funkce jednoho dokladu zastaralá. Protože však existují funkční mezery závislé na této funkci, funkce nezastarají najednou. Místo toho použijeme následující plán: 

- **Vydání z jara 2018** – Tato funkce bude ve výchozím nastavení vypnuta pomocí parametru hlavní knihy. Tuto funkci však můžete zapnout, pokud vaše organizace používá scénář, který spadá do mezer obchodního scénáře, které jsou uvedeny dále v tomto tématu.

  -   Jestliže u odběratele figuruje obchodní scénáře, která nevyžaduje jeden doklad, nezapínejte funkci. Nebudeme opravovat chyby v oblastech, které byly identifikovány dále v tomto tématu, je-li tato funkce použita i v případě, že existuje jiné řešení.

  -   Přestaňte používat Jeden doklad pro integrace do Microsoft Dynamics 365 Finance and Operations, pokud není funkcionalita požadována pro jednu z funkčních mezer.

- **Verze z podzimu 2018 a novějších** – funkční mezery budou doplněny. Po vyplnění funkčních mezer bude funkce jednoho dokladu trvale vypnutá.

- > [!IMPORTANT]
  > Všimněte si, že možnost **pouze jedno číslo dokladu** NEBYLA odebrána z nastavení názvu deníku.  Tato možnost je stále podporována, pokud doklad zahrnuje pouze typy účtů hlavní knihy.  Odběratelé musí být opatrní, když toto nastavení používají, protože doklad se nezaúčtuje v případě, že používají **pouze jedno číslo dokladu**, ale poté zadají více než jednoho odběratele, dodavatele, banku, dlouhodobý majetek nebo projekt.  Odběratelé také mohou zadat kombinaci typů účtů dílčí knihy, například platby v rámci jednoho dokladu, který obsahuje typy účtů dodavatele a banky.  

<a name="why-use-one-voucher"></a>Proč používat Jeden doklad?
====================

Na základě rozhovorů s odběrateli doporučujeme mít kompilován následující seznam scénářů, kde odběratelé používají funkci jednoho dokladu nebo důvodů, proč ho používali. Některé z těchto obchodních požadavků lze splnit pouze pomocí jednoho dokladu. Však mnoho scénářích však alternativy mohou plnit stejné obchodní požadavky.

<a name="scenarios-that-require-one-voucher"></a>Scénáře, které vyžadují jeden doklad
----------------------------------

Následujících scénářů lze dosáhnout pouze pomocí funkce jednoho dokladu. Tyto funkční mezery budou vyplněny pomocí dalších funkcí na podzim 2018 a v novějších verzích.

-   **Zaúčtování plateb dodavatelů v souhrnné formě na bankovní účet**

    -   Organizace komunikuje seznam dodavatelů a částky do jeho banky a banka používá tento seznam pro platby dodavatelů jménem organizace. Banka zaúčtuje součet plateb jako jeden výběr na bankovním účtu.

>   Souhrnu plateb dodavatele je podporován pouze prostřednictvím jednoho dokladu. Každý dodavatel je zadán na samostatném řádku ke správě podrobností v dílčí hlavní knize splatných účtů, ale souhrnná částka všech plateb je odsazená pouze u jednoho řádku pro bankovní účet. Zrušení se tedy zobrazí jako jedna souhrnná částka v dílčí knize banky.

-   Organizace vkládá platby odběratele nebo bankovní vklady plateb odběratele jménem organizace jako paušální částku a na bankovním účtu se zobrazí záloha po uložení.

>   Souhrn plateb odběratele je obvykle podporován prostřednictvím funkce vkladu. Pokud ale používáte "překlenovací" metody platby, v tomto scénáři jsou podporovány pouze v rámci jednoho dokladu. Stejným způsobem, popsaným pro souhrn plateb dodavatele, se zadávají platby odběratele.

-   **Mechanismus k seskupení transakcí z obchodní události**

    -   Organizace má jednu obchodní událost, která spouští několik transakcí. Účetní oddělení však chce zobrazit účetní položky společně, aby bylo možné lépe provádět audit.

>   Pokud organizace musí zobrazit účetní položky z obchodní události společně, musí používat jedno číslo dokladu. 

- **Funkce specifické pro zemi**

  -   Funkce jednoho správního dokumentu (SAD) pro Polsko aktuálně vyžaduje použití jednoho dokladu. Dokud nebude pro tuto funkci možnost seskupení k dispozici , je nutné nadále používat funkci jednoho dokladu. Mohou existovat další funkce specifické pro zemi, které vyžadují funkci jednoho dokladu.

- **Zálohový doklad deníku zákazníka, který má daně na více řádcích**

  -   Odběratel provede zálohu pro objednávku a řádky objednávky mají jiné daně, které musí být zaznamenány pro zálohu. Zálohová platba odběratele je jedna transakce simulující řádky objednávky, aby bylo možné zaznamenat příslušnou daň pro částku na každém řádku.

V tomto případě je zákazník na jednom dokladu stejný vzhledem k tomu, že transakce simuluje řádky objednávky odběratele. Je nutné zadat zálohu do jednoho dokladu, protože výpočet daně musí být proveden na řádcích jedné platby provedené odběratelem.

-   **Údržba dlouhodobého majetku: opravný odpis, rozdělení majetku, výpočet odpisu pro vyřazení**

Následujících transakce dlouhodobého majetku také vytvoří více transakcí v rámci jednoho dokladu:
-   Je provedeno další pořízení dlouhodobého majetku a je vypočten 'opravný' odpis.
-   Majetek je rozdělen.
-   Je povolen parametr k vypočtení odpisu pro vyřazení, a pak je majetek vyřazen.

<a name="scenarios-that-dont-require-one-voucher"></a>Scénáře, které nevyžadují jeden doklad
----------------------------------------

Následujících scénářů lze dosáhnout pomocí jiných prostředků a neměly by používat Jeden doklad.

-   **Zaúčtování plateb odběratelů v souhrnné formě na bankovní účet**

Organizace vkládá platby odběratele nebo bankovní vklady plateb odběratele jménem organizace jako paušální částku a na bankovním účtu se zobrazí záloha po uložení.

Souhrn plateb odběratele je podporován prostřednictvím funkce vkladou, když se u metody platby nepoužívá překlenování.

-   **Určování čistých částek**

V započtení jsou zůstatky dodavatelů a odběratelů vyrovnány s prodejními objednávkami vzájemně vzhledem k tomu, že dodavatel a odběratel představují stejnou stranu. Tento přístup minimalizuje výměnu peněz mezi organizací a stranou odběratele/dodavatele.

Započtení lze provést zadáním zvýšení a snížení v samostatných dokladech a zaúčtování protiúčtu pro zúčtovací účet hlavní knihy.

-   **Zaúčtování souhrnu do hlavní knihy**

Organizace často chtějí účtovat do hlavní knihy souhrnně, aby se minimalizovalo množství dat. Organizace však ještě obvykle vyžadují zachování detaily transakce. Po zaúčtování v souhrnu pomocí jednoho dokladu nejsou známy detaily transakce a nelze je spravovat.

   -   Vzhledem k tomu, že detaily transakce aktuálně nelze spravovat, doporučujeme nepoužívat jeden doklad pro zaúčtování v souhrnu.
   -   Po odstranění podpory jednoho dokladu doporučujeme implementovat architekturu zdrojového dokumentu a účtování do deníků. Tyto architektury budou poté spravovat podrobnosti transakce a podporovat souhrny do hlavní knihy.

-   **Vyrovnání více nezaúčtovaných plateb na stejné faktuře**

K tomuto scénáři obvykle dochází v maloobchodních organizacích, kde mohou odběratelé použít několik metod platby pro zaplacení nákupů. V tomto scénáři musí být organizace schopná zaznamenat více nezaúčtovaných plateb a vyrovnat je proti faktuře odběratele.

Nové funkce, které byly přidány do aplikace Microsoft Dynamics 365 for Operations verze 1611 (listopad 2016) umožňují vypořádat více nezaúčtovaných plateb do vyrovnány u jedné faktury. Vícenásobné platby odběratele se již nezadávají v jednom dokladu.

-   **Import transakcí bankovního výpisu**

Banky často platí a přijímají platby v zastoupení organizace, a tyto transakce se zaznamenávají v modulu Finance and Operations prostřednictvím souboru přijatého od banky. Organizace často chtějí seskupit tyto transakce pomocí čísla bankovního výpisu v souboru. Vzhledem k tomu, že každá transakce je zobrazena podrobně na bankovním výpisu, není požadována žádná sumarizace v dílčí knize banky.

Transakce mohou být seskupeny pomocí dalších polí v deníku, jako je například samotné číslo dávky deníku nebo číslo dokumentu.

-   **Převod zůstatků**

Může být potřeba, aby organizace převedla zůstatek z jednoho dodavatele na jiného dodavatele, buď protože došlo k chybě, nebo proto, že jiný dodavatel převzal zodpovědnost. Převody tohoto typu se také dějí pro typy účtu, jako jsou odběratelé a bankovní účty.

Převody zůstatků z jednoho účtu (dodavatele, odběratele, bankovního účtu a tak dále) na jiný účet a protiúčet lze provádět prostřednictvím samostatných dokladů, a vyrovnání lze zaúčtovat na zúčtovací účet hlavní knihy.

-   **Zadání počátečních zůstatků**

Organizace často zadávají počáteční zůstatky pro účty vedlejší knihy (dodavatelé, odběratelé, dlouhodobého majetku atd.) jako transakce s jedním číslem dokladu. Počáteční zůstatky pro každý účet vedlejší knihy lze zadat jako samostatné doklady a zaúčtovat rozdíl na zúčtovací účet hlavní knihy.

-   **Opravit účetní položky zaúčtovaného dokladu odběratele nebo dodavatele**

Může být nutné, aby organizace opravila účet závazků nebo pohledávek v hlavní knize pro účtování položky zaúčtované faktury, ale tuto fakturu nelze stornovat nebo opravit pomocí jiného mechanismu.

Je-li nutné u pohledávek pro vybrané účty hlavní knihy splatných účtů provést opravu, je nutné provést úpravy přímo do účtu hlavní knihy. Úpravu nelze provést pomocí zaúčtování prostřednictvím odběratele nebo dodavatele. Tento přístup vyžaduje, aby byly provedeny úpravy během prostoje, aby účet hlavní knihy dočasně umožňoval ruční zadávání.

-   **Systém to umožňuje"**

Organizace často používají funkci jednoho dokladu pouze proto, že jim systém umožňuje používat je bez pochopení důsledků.

