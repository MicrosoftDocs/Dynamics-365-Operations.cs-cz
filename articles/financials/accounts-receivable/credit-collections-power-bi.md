---
title: "Obsah správy úvěru a inkasa v Power BI"
description: "Toto téma popisuje, co je součástí obsahu správy úvěru a inkasa v Power BI. Vysvětluje přístup k sestavám Power BI a poskytuje informace o datovém modelu a entitách, které jsou použity k sestavení obsahu."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations. Core
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5f08df6cb8549e87e123b10c5a771ae1c60ff39c
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="credit-and-collections-management-power-bi-content"></a>Obsah správy úvěru a inkasa v Power BI

Toto téma popisuje, co je součástí obsahu **Správa úvěru a inkasa** v Microsoft Power BI. Vysvětluje přístup k sestavám Power BI a poskytuje informace o datovém modelu a entitách, které byly použity k sestavení obsahu.

## <a name="overview"></a>Přehled

Obsah **Správa úvěru a inkasa** v Power BI byl vytvořen pro správce úvěru a inkasa a pro inkasní úředníky. Poskytuje klíčové metriky úvěru a inkasa, jako jsou například počet dnů neuhrazeného prodeje, zůstatek po datu splatnosti, vystavení úvěru a zákazníci, kteří překročili svůj limit úvěru. Používá transakční data a poskytuje agregované zobrazení úvěru a inkasa napříč všemi společnostmi. Také poskytuje rozpis podle společnosti, skupiny odběratelů a odběratele.

Tento obsah Power BI se skládá z 10 stránek sestavy:

- Dvě stránky přehledu (jedna stránka pro přehled úvěru a jednu stránka pro přehled inkasa)
- Osm stránek s podrobnostmi, které obsahují detaily metrik úvěru a inkasa, které jsou rozděleny mezi různé dimenze.

Všechny částky jsou zobrazeny v měně systému. Systémovou měnu můžete nastavit na stránce **Parametry systému**.

Ve výchozím nastavení se zobrazují data úvěrů a inkas pro aktuální společnost. Abyste zobrazili data napříč všemi společnostmi, přiřaďte funkční oprávnění **CustCollectionsBICrossCompany** k roli.

## <a name="accessing-the-power-bi-content"></a>Přístup k obsahu Power BI
Pokud používáte aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (červenec 2017), zobrazuje se **Správa úvěru a inkasa** Power BI v pracovním prostoru **Úvěr a inkasa odběratele**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Sestavy, které jsou součástí obsahu Power BI

Obsah **CustCollectionsBICrossCompany** Power BI obsahuje sestavu, která sestává ze sady metrik. Tyto metriky jsou zobrazována jako grafy, dlaždice a tabulky. Následující tabulka poskytuje přehled vizualizací v obsahu **CustCollectionsBICrossCompany** v Power BI.

| Stránka sestavy                 | Vizualizace |
|-----------------------------|---------------|
| Přehled inkas        | <ul><li>Odběratelé po splatnosti</li><li>Odběratelé s překročeným úvěrovým limitem</li><li>DSO 30 dní</li><li>Otevřené případy</li><li>Průměrný počet dní do uzavření případu</li><li>Otevřené aktivity</li><li>Průměrný počet dní do uzavření aktivit</li><li>Otevřít oznámení úroků</li><li>Otevřít upomínky</li><li>Blokování odběratele</li><li>Blokování prodeje</li><li>Splatné zůstatky</li><li>Částky stavu inkasa</li><li>Částky kódu inkasa</li><li>Odpis podle důvodu</li><li>Splatný zůstatek podle oblasti</li><li>Očekávané platby</li></ul> |
| Přehled úvěru             | <ul><li>Odběratelé po splatnosti</li><li>Limit úvěru a splatný zůstatek</li><li>Mřížka odběratelů s překročeným limitem úvěru</li><li>Odběratelé s překročeným úvěrovým limitem podle společnosti</li><li>Použitý úvěr a celkový limit úvěru</li><li>Limit úvěru a použitý úvěr podle oblasti</li><li>Odběratelé podle úvěruschopnosti</li></ul> |
| Limit úvěru                | <ul><li>Limit úvěru</li><li>Podrobnosti limitu úvěru</li><li>Limit úvěru podle odběratele</li><li>Limit úvěru podle skupiny odběratelů</li><li>Limit úvěru podle úvěruschopnosti společnosti</li><li>Limit úvěru oproti použitému úvěru podle oblasti</li></ul> |
| Odběratelé s překročeným úvěrovým limitem | <ul><li>Odběratelé s překročeným úvěrovým limitem</li><li>Podrobnosti odběratelů s překročeným limitem úvěru</li><li>Odběratelé s překročeným úvěrovým limitem podle společnosti</li><li>Odběratel s překročeným limitem úvěru podle skupiny odběratelů</li><li>Odběratelé s překročeným úvěrovým limitem podle regionu</li></ul> |
| Odběratelé po splatnosti          | <ul><li>Odběratelé po splatnosti</li><li>Podrobnosti odběratele po splatnosti</li><li>Odběratel po splatnosti podle společnosti</li><li>Odběratel po splatnosti podle skupiny odběratelů</li><li>Odběratel po splatnosti podle oblasti</li></ul> |
| Splatné zůstatky               | <ul><li>Splatné zůstatky</li><li>Podrobnosti splatných zůstatků</li><li>Splatné zůstatky podle společnosti</li><li>Splatné zůstatky podle skupiny odběratelů</li></ul> |
| Očekávané platby           | <ul><li>Očekávané platby</li><li>Podrobnosti očekávaných plateb</li><li>Očekávané platby podle společnosti</li><li>Očekávané platby podle skupiny odběratelů</li><li>Očekávané platby podle oblasti</li></ul> |
| Odpisy                  | <ul><li>Odpisy podle oblasti</li><li>Podrobnosti odpisů</li><li>Odpisy podle hlavního účtu</li><li>Odpisy podle společnosti</li><li>Odpisy podle skupiny odběratelů</li><li>Odpisy podle oblasti</li></ul> |
| Stav inkasa          | <ul><li>Sporné</li><li>Slib zaplacení porušen</li><li>Přislíbit zaplacení</li><li>Podrobnosti stavu inkasa</li><li>Částky stavu inkasa</li><li>Otevřené případy</li><li>Otevřené aktivity</li></ul> |
| Upomínky         | <ul><li>Částky kódu výběru</li><li>Podrobnosti částky kódu inkasa</li><li>Částka upomínky podle společnosti</li><li>Částka upomínky podle skupiny odběratelů</li><li>Částka upomínky podle oblasti</li></ul> |

Grafy a dlaždice ve všech těchto sestavách můžete filtrovat a ukotvit na řídicím panelu. Další informace o filtrování a ukotvení v aplikaci Power BI naleznete v tématu [Vytvoření a konfigurace řídicího panelu](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Můžete také použít základní funkci exportu dat pro export základních dat, jejichž souhrn je uveden na vizualizaci.

## <a name="extending-the-power-bi-content"></a>Rozšíření obsahu v Power BI
Pomocí balíčků obsahu, které jsou k dispozici ve službě Microsoft Dynamics Lifecycle Services (LCS) můžete poskytovat skvělou analýzu osobám, které nejsou přihlášeny k aplikaci Finance and Operations. Tyto balíčky obsahu můžete upravit tak, aby zahrnovaly jiné sestavy nebo vizuály, a potom publikovat balíčky obsahu na svého klienta Power BI.com pro analýzu.

Obsah **Správa úvěru a inkasa** v Power BI naleznete v knihovně sdíleného majetku ve službě LCS. Další informace o stažení obsahu a jeho implementaci ve vaší organizaci naleznete v tématu [Obsah Power BI v LCS od společnosti Microsoft a vašich partnerů](../../dev-itpro/analytics/power-bi-content-microsoft-partners.md). Pokud se chcete podívat na ukázku, jak implementovat obsah Power BI, najdete informace v tématu [Obsah Power BI od společnosti Microsoft a partnerů ve službě Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) pro Office Mix.

Nezapomeňte si stáhnout obsah **Správa úvěru a inkasa** v Power BI, který se vztahuje k vámi používané verzi aplikace Finance and Operations.

## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách

Následující data se používají k naplnění stránek sestavy v obsahu **Správa úvěru a inkasa** v Power BI. Tato data jsou vyjádřena jako agregační měření, která jsou rozfázována v úložišti entit. Úložiště entit je databáze Microsoft SQL Server, která je optimalizována pro analýzu. Další informace naleznete v tématu [Přehled integrace Power BI úložištěm entit](../../dev-itpro/analytics/power-bi-integration-entity-store.md).

| Celek                                      | Klíčová opatření agregace           | Zdroj dat                                 | Pole                                                      | popis |
|---------------------------------------------|--------------------------------------|---------------------------------------------|------------------------------------------------------------|-------------|
| CustCollectionsBIActivitiesAverageCloseTime | NumOfActivities, AveragecClosedTime  | smmActivities                               | AverageOfChildren(AverageClosedTime) Count(ActivityNumber) | Počet uzavřených aktivit a průměrná doba k uzavření těchto aktivit. |
| CustCollectionsBIActivitiesOpen             | ActivityNumber                       | smmActivities                               | Count(ActivityNumber)                                      | Počet otevřených aktivit. |
| CustCollectionsBIAgedBalances               | AgedBalances                         | CustCollectionsBIAgedBalancesView           | Sum(SystemCurrencyBalance)                                 | Součet splatných zůstatků. |
| CustCollectionsBIBalancesDue                | SystemCurrencyAmount                 | CustCollectionsBIBalanceDueView             | Sum(SystemCurrencyAmount)                                  | Částky, které jsou po splatnosti. |
| CustCollectionsBICaseAverageCloseTIme       | NumOfCases, CaseAverageClosedTime    | CustCollectionsCaseDetail                   | AverageOfChildren(CaseAverageClosedTime) Count(NumOfCases) | Počet uzavřených případů a průměrná doba k uzavření těchto případů. |
| CustCollectionsBICasesOpen                  | CaseId                               | CustCollectionsCaseDetail                   | Count(CaseId)                                              | Počet otevřených případů. |
| CustCollectionsBICollectionLetter           | CollectionLetterNum                  | CustCollectionLetterJour                    | Count(CollectionLetterNum)                                 | Počet otevřených upomínek. |
| CustCollectionsBICollectionLetterAmount     | CollectionLetterAmounts              | CustCollectionsBIAccountsReceivables        | Sum(SystemCurrencyAmount)                                  | Zůstatek zaúčtovaných upomínek. |
| CustCollectionsBICollectionStatus           | CollectionStatusAmounts              | CustCollectionsBIAccountsReceivables        | Sum(SystemCurrencyAmount)                                  | Zůstatek transakce se stavem inkasa. |
| CustCollectionsBICredit                     | CreditExposed, AmountOverCreditLimit | CustCollectionsBICreditView                 | Sum(CreditExposed), Sum(AmountOverCreditLimit)             | Součet vystavení úvěru a částek, o které odběratelé překročili limit úvěru. |
| CustCollectionsBICustOnHold                 | Blokováno                              | CustCollectionsBICustTable                  | Count(Blocked)                                             | Počet odběratelů, kteří jsou blokováni. |
| CustCollectionsBIDSO                        | DSO30                                | CustCollectionsBIDSOView                    | AverageOfChildren(DSO30)                                   | Počet dnů neuhrazeného prodeje pro 30 dnů. |
| CustCollectionsBIExpectedPayment            | ExpectedPayment                      | CustCollectionsBIExpectedPaymentView        | Sum(SystemCurrencyAmounts)                                 | Součet očekávaných plateb v rámci dalšího roku. |
| CustCollectionsBIInterestNote               | InterestNote                         | CustInterestJour                            | Count(InterestNote)                                        | Počet oznámení úroků, která byly vytvořeny. |
| CustCollectionsBISalesOnHold                | SalesId                              | SalesTable                                  | Count(SalesId)                                             | Počet celkových prodejních objednávek, které jsou blokovány. |
| CustCollectionsBIWriteOff                   | WriteOffAmount                       | CustCollectionsBIWriteOffView               | Sum(SystemCurrencyAmount)                                  | Součet transakcí, které byly odepsány. |

