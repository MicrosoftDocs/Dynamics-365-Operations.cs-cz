---
title: Konfigurace vyrovnání
description: To, jak a kdy jsou transakce vyrovnány, může být poměrně složité, proto je nutné pochopit a správně definovat parametry pro splnění požadavků společnosti. Tento článek popisuje parametry, které se používají k vyrovnání pro závazky i pohledávky.
author: kweekley
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, CustParameters, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 14601
ms.assetid: 6b61e08c-aa8b-40c0-b904-9bca4e8096e7
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14ed2999a9ad8ffc64815ca3f8b1556aad27ae48
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910193"
---
# <a name="configure-settlement"></a>Konfigurace vyrovnání

[!include [banner](../includes/banner.md)]

To, jak a kdy jsou transakce vyrovnány, může být poměrně složité, proto je nutné pochopit a správně definovat parametry pro splnění požadavků společnosti. Tento článek popisuje parametry, které se používají k vyrovnání pro závazky i pohledávky. 

Následující parametry ovlivní způsob zpracování vyrovnání v aplikaci Microsoft Dynamics 365 Finance. Vyrovnání je proces vyrovnání faktury podle platbou nebo dobropisem. Tyto parametry jsou umístěny v oblasti **Vyrovnání** stránek **Parametry pohledávek** a **Parametry závazků**.

- **Automatické vyrovnání** – nastavte možnost na hodnotu **Ano**, má-li se transakce automaticky vyrovnat oproti otevřeným transakcím při zaúčtování. Je-li tato možnost je nastavena na hodnotu **Ne**, uživatelé mohou transakce vyrovnat ručně při zadávání plateb nebo později pomocí stránky **Vyrovnat transakce**.
- **Správa platební slevy** – zadejte způsob [zpracování platební slevy při přeplacení faktury](cash-discount-handling-overpayments.md). U přeplatku lze platební slevu snížit, považovat za rozdíl nebo ponechat na účtu pro dodavatele nebo odběratele.
  -   **Neurčeno** – částka platební slevy se sníží o částku přeplatku. Toto chování se vždy používá bez ohledu na to, zda je částka přeplatku větší nebo menší než částka zadaná v poli **Maximální přeplatek či nedoplatek**.
  -   **Specifické** – částka přeplatku buď je zaúčtována na účet hlavní knihy s rozdílem platební slevy, nebo zůstane zůstatek na účtu odběratele nebo dodavatele. Specifické chování závisí na tom, zda je částka přeplatku mezi 0,00 a částkou zadanou v poli **Maximální přeplatek či nedoplatek**, nebo zda je částka přeplatku větší než částka **Maximální přeplatek či nedoplatek**.
- **Maximální haléřový rozdíl** – zadejte maximální povolený haléřový rozdíl pro vyrovnané transakce. Je-li rozdíl menší nebo rovný haléřovému rozdílu určenému v tomto poli, rozdíl se zaúčtuje na účet haléřových rozdílů v hlavní knize uvedený na stránce **Účty pro automatické transakce**.
- **Maximální přeplatek či nedoplatek** – zadejte částku, která se přijme jako přeplatek a nedoplatek. Chcete-li vypočítat daň u přeplatků či nedoplatků, na stránce **Parametry hlavní knihy** klikněte na volbu **DPH** a zvolte možnost **DPH při nedoplatku nebo přeplatku**.
  -   Pokud přeplatek či nedoplatek tvoří rozdíl menší než je rozdíl určený v poli **Maximální haléřový rozdíl**, částka haléřového rozdílu bude zaúčtována na účet haléřových rozdílů
  -   Pokud přeplatek či nedoplatek tvoří rozdíl větší než je rozdíl určený v poli **Maximální haléřový rozdíl**, částka rozdílu bude zaúčtována na účet rozdílů vybraný pro typ zaúčtování **Platební sleva odběratele** nebo **Platební sleva dodavatele** na stránce **Účty pro automatické transakce**.
- **Vypočítat platební slevy pro částečné platby** – nastavte možnost na hodnotu **Ano**, chcete-li povolit, aby se platební slevy automaticky vypočítávaly pro částečné platby.
  -   Účinek této možnosti závisí na hodnotě v poli **Použít platební slevu** na stránce **Vyrovnat transakce**. Je-li tato možnost je nastavena na hodnotu **Ano**, sleva je přijata při nastavení pole **Použít platební slevy** na hodnotu **Normální**. Pokud je pole **Použít platební slevy** nastaveno na hodnotu **Vždy**, platební sleva je vždy přijata bez ohledu na nastavení v tomto poli. Pokud je pole **Použít platební slevu** nastaveno na hodnotu **Vždy**, platební sleva je vždy přijata bez ohledu na nastavení v tomto poli.
  -   Je-li tato možnost nastavena na hodnotu **Ano** a uživatel změní hodnot v poli **Částka k vyrovnání** na stránce **Vyrovnat transakce**, sleva se vypočítá automaticky a bude zobrazena jako výchozí hodnota v poli **Částka platební slevy k přijetí**.
  -   Je-li tato možnost nastavena na hodnotu **Ne** a uživatel provede změnu hodnoty v poli **Částka k vyrovnání** na stránce **Vyrovnat transakce**, jako výchozí hodnota v poli **Částka platební slevy k přijetí** se použije hodnota **0** (nula).
- **Vypočítat platební slevy pro dobropisy** – nastavte možnost na hodnotu **Ano**, aby se automaticky vypočítala platební sleva pro dobropisy. V části Pohledávky je transakce dobropisu záporná transakce s hodnotou v poli **Faktura** na stránce **Volná faktura** nebo vrácení na stránce **Prodejní objednávka**.
  - Účinek této možnosti závisí na hodnotě v poli <strong>Použít platební slevu</strong> na stránce <strong>Vyrovnat transakce</strong>. Je-li tato možnost je nastavena na hodnotu <strong>Ano</strong>, sleva je přijata při nastavení pole *<strong><em>Použít platební slevy</em></strong>* na hodnotu <strong>Normální</strong>. Pokud je pole *<strong><em>Použít platební slevy</em></strong>* nastaveno na hodnotu <strong>Vždy</strong>, platební sleva je vždy přijata bez ohledu na nastavení v tomto poli. Pokud je pole *<strong><em>Použít platební slevu</em></strong>* nastaveno na hodnotu <strong>Nikdy</strong>, platební sleva není nikdy přijata bez ohledu na nastavení v tomto poli.
  - Je-li tato možnost nastavena na hodnotu **Ano** a dobropis je označený na stránce **Vyrovnat transakce**, sleva se vypočítá automaticky a bude zobrazena jako výchozí hodnota v poli **Částka platební slevy k přijetí**.
  - Je-li tato možnost nastavena na hodnotu **Ne** a dobropis je označený na stránce **Vyrovnat transakce**, bude jako výchozí hodnota v poli **Částka platební slevy k přijetí** použita hodnota **0** (nula).

- **Slevové protiúčty (pouze závazky)** – definujte výchozí účetní knihy platebních slev, která má být použita pro účetní položku pro platební slevy.
  -   **Použít hlavní účet slev pro dodavatele** – platební sleva je zaúčtována pro hlavní účet, který je definován na stránce **Nastavení platební slevy**.
  -   **Účty na řádcích faktury** – platební sleva je zaúčtována na účty hlavní knihy pro původní fakturu.
- **Označit řádky na volných fakturách a oznámeních úroků (pouze pohledávky)** – nastavte možnost na hodnotu **Ano**, abyste aktivovali tlačítko **Označit řádky faktury** na stránkách **Zadat platby odběratele**, **Platební doklad deníku** a **Vyrovnat transakce**. Toto tlačítko umožňuje označit jednotlivé řádky pro vyrovnání.
- **Určit prioritu vyrovnání (pouze pohledávky)** – nastavte možnost na hodnotu **Ano**, abyste aktivovali tlačítko **Označit podle priority** na stránkách **Zadat platby odběratele** a **Vyrovnat transakce**. Toto tlačítko umožňuje uživatelům přiřadit k transakcím předem stanovené pořadí vyrovnání.  Po použití pořadí vyrovnání na transakci lze upravit pořadí a přidělení platby před zaúčtováním.
- **Použít prioritu pro automatické vyrovnání** – nastavte tuto možnost na **Ano**, chcete-li použít definované pořadí priority při automatickém vyrovnání transakcí. Toto pole je k dispozici pouze tehdy, pokud jsou volby **Určit prioritu vyrovnání** a **Automatické vyrovnání** nastaveny na hodnotu **Ano**.

## <a name="fixed-dimensions-on-accounts-receivableaccounts-payable-main-accounts"></a>Pevné dimenze na hlavních účtech pohledávek/ závazků

Když se na hlavním účtu pohledávek / závazků používají pevné dimenze, budou při procesu vyrovnání zaúčtovány další účetní záznamy a dvě další dodavatelské transakce. vyrovnání porovná účet hlavní knihy pohledávek a závazků z faktury a platby.  Když jsou platby a vyrovnání dokončeny dohromady, což je typický scénář, účetní zápis platby nebyla zaúčtován do hlavní knihy, pokud není dokončen také proces vyrovnání. Z důvodu pořadí zpracování událostí vyrovnání nedokáže určit skutečný účet hlavní knihy pohledávek/závazků z účetního zápisu platby v hlavní knize. Vyrovnání rekonstruuje, jaký účet hlavní knihy bude pro platbu určen. Toto číslo se stává problémem při použití pevné dimenze pro hlavní účet pohledávek a účet závazků.

Aby bylo možné rekonstruovat účet hlavní knihy, je hlavní účet pohledávek a závazků načten z účetního profilu a finanční dimenze jsou načteny ze záznamu transakce dodavatele pro platbu, jak je definováno v deníku plateb. Pevné dimenze nejsou ve výchozím nastavení poslány do deníků plateb, ale namísto toho platí pro hlavní účet jako poslední krok procesu zaúčtování. V důsledku toho nebude hodnota pevné dimenze pravděpodobně obsažena v transakci dodavatele, pokud není dodána z jiného zdroje, jako je dodavatel. Rekonstruovaný účet nebude zahrnovat pevnou dimenzi. Zpracování vyrovnání určí, že musí být vytvořena položka vyrovnání, protože faktura byla zaúčtovaná s pevnou hodnotou dimenze a rekonstruovaný účet platby nebyl.  Jak vyrovnání pokračuje zaúčtováním upravující položky, použije se poslední krok při zaúčtování pevné dimenze. Přidáním pevné dimenze k vyrovnávací položce je zaúčtován s částkou Má dáti a Dal na stejný účet hlavní knihy. Vyrovnání nemůže vrátit zpět účetní položky.

Abyste se vyhnuli dalším účetním položkám, straně Má dáti a Dal na stejném účtu hlavní knihy, měla by být vzata v úvahu následující zástupná řešení v závislosti na obchodních požadavcích. 

-   Organizace často používají pevné dimenze k nulovému plnění a finanční dimenzi, která není požadována. Obvykle se jedná o případy pro rozvahové účty, jako jsou účty pohledávek a závazků. Účetní struktury lze použít pro nesledované finanční dimenze, které jsou obvykle vyplněny nulovými hodnotami.  Odebrání finanční dimenze pro rozvahové účty eliminuje nutnost použít pevné dimenze.
-   Pokud vaše organizace vyžaduje pevné dimenze na hlavním účtu pohledávek/závazků, najděte způsob nastavení výchozí pevné dimenze pro platbu, tak, aby hodnota pevné dimenze byla uložena v transakci dodavatele pro platbu. To umožní systému obnovit hlavní účet pohledávek a závazků tak, aby zahrnoval hodnoty pevné dimenze. Hodnotu pevné dimenze lze definovat jako výchozí pro dodavatele nebo pro název deníku pro deník plateb.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
