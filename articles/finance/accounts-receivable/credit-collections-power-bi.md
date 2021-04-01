---
title: Obsah správy úvěru a inkasa v Power BI
description: Toto téma popisuje, co je součástí obsahu správy úvěru a inkasa v Power BI. Vysvětluje přístup k sestavám Power BI a poskytuje informace o datovém modelu a entitách, které byly použity k sestavení obsahu.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: dfa79b3fb4099d64390c17b39508deaac63deb1c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235154"
---
# <a name="credit-and-collections-management-power-bi-content"></a>Obsah správy úvěru a inkasa v Power BI

[!include [banner](../includes/banner.md)]

Toto téma popisuje, co je součástí obsahu **správy úvěru a inkasa** v Microsoft Power BI. Vysvětluje přístup k sestavám Power BI a poskytuje informace o datovém modelu a entitách, které byly použity k sestavení obsahu.

## <a name="overview"></a>Přehled

**Obsah Správa úvěru a inkasa** v Power BI byl vytvořen pro správce úvěru a inkasa a pro inkasní úředníky. Poskytuje klíčové metriky úvěru a inkasa, jako jsou například počet dnů neuhrazeného prodeje, zůstatek po datu splatnosti, vystavení úvěru a zákazníci, kteří překročili svůj limit úvěru. Používá transakční data a poskytuje agregované zobrazení úvěru a inkasa napříč všemi společnostmi. Také poskytuje rozpis podle společnosti, skupiny odběratelů a odběratele.

Tento obsah Power BI se skládá z 10 stránek sestavy:

- Dvě stránky přehledu (jedna stránka pro přehled úvěru a jednu stránka pro přehled inkasa)
- Osm stránek s podrobnostmi, které obsahují detaily metrik úvěru a inkasa, které jsou rozděleny mezi různé dimenze.

Všechny částky jsou zobrazeny v měně systému. Systémovou měnu můžete nastavit na stránce **Parametry systému**.

Ve výchozím nastavení se zobrazují data úvěrů a inkas pro aktuální společnost. Abyste zobrazili data napříč všemi společnostmi, přiřaďte funkční oprávnění **CustCollectionsBICrossCompany** k roli.

## <a name="setup-needed-to-view-power-bi-content"></a>Zobrazení obsahu Power BI vyžaduje instalační programu

Následující nastavení je nutné dokončit, aby bylo možné zobrazit data ve vizuálech **Obrázky a kolekce kreditů** Power BI .

1. Přejděte na **Správa systému > Nastavení > Systémové parametry** a nastavte hodnoty **Měna systému** a **Směnný kurz systému**.
2. Přejděte na **Hlavní kniha > Kalendáře > Fiskální kalendáře** k ověření dat fiskálního kalendáře přiřazených k aktivnímu časovému období.
3. Přejděte na **Hlavní kniha > Nastavení > Účetní kniha** a nastavte **Měna účtování** a **Typ směnného kurzu**.
4. Definujte směnné kurzy mezi měnami transakcí a zúčtovací měnou, zúčtovací měnu a systémovou měnou. Postup: Přejděte na: **Hlavní kniha > Měny > Směnné kurzy měn**.
5. Přejděte na **Správa systému > Nastavení > Úložiště Entit**, pokud chcete aktualizovat agregované měření **CustCollectionsBIMeasurementsV2**.

>[!NOTE] 
> Definice období stárnutí musí být nastaveny v **Parametrech pohledávek > Kolekce > Výchozí kolekce**, chcete-li umožnit data stárnutí v obsahu Power BI.

## <a name="accessing-the-power-bi-content"></a>Přístup k obsahu Power BI

Obsah **Správa kreditu a inkasa** v Power BI se zobrazí v pracovním prostoru **Kredit a inkasa odběratele**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Sestavy, které jsou součástí obsahu Power BI

Obsah **CustCollectionsBICrossCompany** v Power BI obsahuje sestavu, která sestává ze sady metrik. Tyto metriky jsou zobrazována jako grafy, dlaždice a tabulky. Následující tabulka poskytuje přehled vizualizace v obsahu **CustCollectionsBICrossCompany** v Power BI.

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

Grafy a dlaždice ve všech těchto sestavách můžete filtrovat a ukotvit na řídicím panelu. Další informace o filtrování a ukotvení v Power BI naleznete v tématu [Vytvoření a konfigurace řídicího panelu](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Můžete také použít základní funkci exportu dat pro export základních dat, jejichž souhrn je uveden na vizualizaci.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]