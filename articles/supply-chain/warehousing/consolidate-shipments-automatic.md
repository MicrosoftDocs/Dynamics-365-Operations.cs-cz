---
title: Konsolidace dodávek při uvolnění do skladu pomocí automatického uvolnění prodejních objednávek
description: Tento článek představuje scénář, ve kterém je více objednávek uvolněno do skladu ve stejném periodickém postupu automatizovaného uvolnění do skladu.
author: Mirzaab
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: ba8e9790a5b7eb00b20fba19f452118e1f05fed0
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428247"
---
# <a name="consolidate-shipments-released-to-the-warehouse-using-automatic-release-of-sales-orders"></a>Konsolidace dodávek při uvolnění do skladu pomocí automatického uvolnění prodejních objednávek

[!include [banner](../includes/banner.md)]

Tento článek představuje scénář, ve kterém je více objednávek uvolněno do skladu ve stejném periodickém postupu automatizovaného uvolnění do skladu. Objednávky budou automaticky konsolidovány do dodávek na základě pravidel definovaných jako zásady konsolidace dodávek.

Během scénáře vytvoříte sady prodejních objednávek a uvolníte každou sadu do skladu. Poté zkontrolujete dodávky, které jsou vytvořeny nebo aktualizovány během konsolidace dodávek, na základě nakonfigurovaných zásad.

## <a name="make-demo-data-available"></a>Zpřístupnění ukázkových dat

Scénář v tomto článku odkazuje na hodnoty a záznamy, které jsou součástí standardních ukázkových dat poskytovaných pro aplikaci Microsoft Dynamics 365 Supply Chain Management. Pokud chcete při cvičení použít hodnoty, které jsou zde uvedeny, nezapomeňte pracovat v prostředí, ve kterém jsou nainstalovaná ukázková data, a nastavte právnickou osobu na **USMF**, než začnete.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Nastavení zásad konsolidace dodávek a filtry produktů

Scénář, který je zde popsán, předpokládá, že jste již tuto funkci zapnuli a provedli cvičení v [konfiguraci zásad konsolidace dodávek](configure-shipment-consolidation-policies.md) a vytvořili zásady a další záznamy, které jsou zde popsány. Než budete pokračovat v tomto scénáři, nezapomeňte tato cvičení provést.

## <a name="create-the-sales-orders-for-this-scenario"></a>Vytvoření prodejních objednávek pro tento scénář

Začněte vytvořením kolekce prodejních objednávek, se kterou můžete pracovat. Musíte pracovat se skladem, který je povolen pro rozšířené procesy skladu (WMS). Pokud není výslovně uveden jiný sklad, musí být stejný sklad použit pro každou z následujících sad objednávek.

Přejděte na **Pohledávky \> Objednávky \> Všechny prodejní objednávky** a vytvořte kolekci prodejních objednávek, jejichž nastavení jsou popsána v následujících pododdílech.

### <a name="create-order-set-1"></a>Vytvoření sady objednávek 1

#### <a name="sales-order-1-1"></a>Prodejní objednávka 1-1

1. Vytvořte prodejní objednávku, která má následující nastavení:

    - **Účet zákazníka:** *US-001*
    - **Způsob doručení:** *Airwa-Air*

1. Přidejte řádek objednávky, který má následující nastavení:

    - **Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)
    - **Množství:** *1.00*

#### <a name="sales-order-1-2"></a>Prodejní objednávka 1-2

1. Vytvořte prodejní objednávku, která má následující nastavení:

    - **Účet zákazníka:** *US-001*
    - **Způsob doručení:** *Airwa-Air*

1. Přidejte řádek objednávky, který má následující nastavení:

    - **Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)
    - **Množství:** *1.00*

#### <a name="sales-order-1-3"></a>Prodejní objednávka 1-3

1. Vytvořte prodejní objednávku, která má následující nastavení:

    - **Účet zákazníka:** *US-001*
    - **Způsob dodání:** *10*

1. Přidejte řádek objednávky, který má následující nastavení:

    - **Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)
    - **Množství:** *1.00*

1. Přidejte druhý řádek objednávky, který má následující nastavení:

    - **Číslo položky:** *A0002* (položka, ke které není přiřazen filtr **Kód 4**)
    - **Množství:** *1.00*
    - **Způsob doručení:** *Airwa-Air*

### <a name="create-order-set-2"></a>Vytvoření sady objednávek 2

#### <a name="sales-orders-2-1-and-2-2"></a>Prodejní objednávky 2-1 a 2-2

1. Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:

    - **Účet zákazníka:** *US-002*

1. Přidejte řádek objednávky, který má následující nastavení:

    - **Číslo položky:** *M9200* (položka, kde je filtr **Kód 4** nastaven na *Hořlavý*)
    - **Množství:** *1.00*

1. Přidejte druhý řádek objednávky, který má následující nastavení:

    - **Číslo položky:** *M9201* (položka, kde je filtr **Kód 4** nastaven na *Explozivní*)
    - **Množství:** *1.00*
    - **Způsob doručení:** *Airwa-Air*

### <a name="create-order-set-3"></a>Vytvoření sady objednávek 3

#### <a name="sales-order-3-1"></a>Prodejní objednávka 3-1

1. Vytvořte prodejní objednávku, která má následující nastavení:

    - **Účet zákazníka:** *US-002*

1. Přidejte řádek objednávky, který má následující nastavení:

    - **Číslo položky:** *M9200* (položka, kde je filtr **Kód 4** nastaven na *Hořlavý*)
    - **Množství:** *1.00*

1. Přidejte druhý řádek objednávky, který má následující nastavení:

    - **Číslo položky:** *M9201* (položka, kde je filtr **Kód 4** nastaven na *Explozivní*)
    - **Množství:** *1.00*
    - **Způsob doručení:** *Airwa-Air*

> [!NOTE]
> Tato objednávka je totožná se dvěma objednávkami, které jste vytvořili pro sadu objednávek 2. Je však uvedena jako vlastní sada objednávek, protože ji později v tomto scénáři uvolníte samostatně.

### <a name="create-order-set-4"></a>Vytvoření sady objednávek 4

#### <a name="sales-order-4-1"></a>Prodejní objednávka 4-1

1. Vytvořte prodejní objednávku, která má následující nastavení:

    - **Účet zákazníka:** *US-001*
    - **Žádost zákazníka:** *1*

1. Přidejte řádek objednávky, který má následující nastavení:

    - **Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)
    - **Množství:** *1.00*

### <a name="create-order-set-5"></a>Vytvoření sady objednávek 5

#### <a name="sales-orders-5-1-and-5-2"></a>Prodejní objednávky 5-1 a 5-2

1. Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:

    - **Účet zákazníka:** *US-001*
    - **Žádost zákazníka:** *2*

1. Přidejte řádek objednávky, který má následující nastavení:

    - **Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)
    - **Množství:** *1.00*

#### <a name="sales-order-5-3"></a>Prodejní objednávka 5-3

1. Vytvořte prodejní objednávku, která má následující nastavení:

    - **Účet zákazníka:** *US-001*
    - **Žádost zákazníka:** *1*

1. Přidejte řádek objednávky, který má následující nastavení:

    - **Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)
    - **Množství:** *1.00*

### <a name="create-order-set-6"></a>Vytvoření sady objednávek 6

#### <a name="sales-orders-6-1-and-6-2"></a>Prodejní objednávky 6-1 a 6-2

1. Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:

    - **Účet zákazníka:** *US-003*
    - **Žádost zákazníka:** *2*

1. Přidejte řádek objednávky, který má následující nastavení:

    - **Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)
    - **Množství:** *1.00*

#### <a name="sales-orders-6-3-and-6-4"></a>Prodejní objednávky 6-3 a 6-4

1. Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:

    - **Účet zákazníka:** *US-004*
    - **Žádost zákazníka:** *1*

1. Přidejte řádek objednávky, který má následující nastavení:

    - **Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)
    - **Množství:** *1.00*

#### <a name="sales-orders-6-5-and-6-6"></a>Prodejní objednávky 6-5 a 6-6

1. Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:

    - **Účet zákazníka:** *US-007*
    - **Lokalita:** *6*
    - **Sklad:** *61*
    - **Fond:** *ShipCons*

1. Přidejte řádek objednávky, který má následující nastavení:

    - **Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)
    - **Množství:** *1.00*

#### <a name="sales-orders-6-7-and-6-8"></a>Prodejní objednávky 6-7 a 6-8

1. Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:

    - **Účet zákazníka:** *US-007*
    - **Lokalita:** *6*
    - **Sklad:** *61*
    - **Fond:** Pole ponechejte prázdné.

1. Přidejte řádek objednávky, který má následující nastavení:

    - **Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)
    - **Množství:** *1.00*

## <a name="automatic-release-of-sales-orders-to-the-warehouse"></a>Automatické uvolnění prodejních objednávek do skladu

U každé sady prodejních objednávek, které jste vytvořili dříve, dokončíte postup automatického uvolnění do skladu. V každém případě budete pracovat prostřednictvím [základního postupu uvolnění do skladu](#release-procedure), který je uveden zde.

### <a name="basic-release-to-warehouse-procedure"></a><a name="release-procedure"></a>Základní postup uvolnění do skladu

U každé sady prodejních objednávek, které jste vytvořili dříve, dokončíte tři postupy, které jsou popsány v následujících pododdílech.

#### <a name="update-the-wave-template-that-will-be-used-during-release"></a>Aktualizace šablony vln, která bude použita během uvolnění

1. Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Šablony vlny**.
1. Nastavte pole **Typ šablony vln** na *Expedice*.
1. Najděte a vyberte šablonu vlny přidruženou ke skladu, který jste použili v sadách objednávek, které jste pro tento scénář vytvořili. Pokud jste například použili sklad *24*, vybere šablonu vlny **Výchozí expedice 24**. Pokud jste použili sklad *61*, vybere šablonu vlny **Expedice 61**.
1. V podokně akcí vyberte **Upravit**.
1. Nastavte možnost **Zpracovat vlnu při uvolnění do skladu** na *Ne*.

#### <a name="release-to-the-warehouse"></a>Uvolnění do skladu

1. Přejděte na **Řízení skladu \> Uvolnění do skladu \> Automatické uvolnění prodejních objednávek**.
1. Nastavte pole **Množství k uvolnění** na *Vše*.
1. Na záložce s náhledem **Záznamy k zahrnutí** vyberte **Filtr** a otevřete dialogové okno dotazu.
1. Na kartě **Rozsah** vyberte **Přidat** a přidejte do mřížky řádek, který má následující nastavení:

    - **Tabulka:** *Prodejní objednávka*
    - **Odvozená tabulka:** *Prodejní objednávka*
    - **Pole:** *Prodejní objednávka*
    - **Kritéria:** Zadejte čárkami oddělený seznam čísel prodejních objednávek z požadované sady objednávek.

1. Vyberte **OK** a uložte dotaz.
1. Vyberte **OK** a zahajte postup *Automatické uvolnění do skladu*.

#### <a name="review-the-shipment-that-is-created-or-updated"></a>Kontrola dodávky, která je vytvořena nebo aktualizována

1. Přejděte na **Řízení skladu \> Dodávky \> Všechny dodávky**.
1. Najděte a vyberte požadovanou dodávku.
1. Pokud byla při vytváření nebo aktualizaci dodávky použita zásada konsolidace, měli byste ji vidět v poli **Zásada konsolidace dodávek**.

### <a name="release-sales-orders-from-order-set-1"></a>Uvolnění prodejních objednávek ze sady objednávek 1

Následujte [základní postup uvolnění do skladu](#release-procedure) a uvolněte prodejní objednávky ze sady objednávek 1.

Po dokončení byste měli vidět, že byly vytvořeny dvě dodávky:

- První dodávka obsahuje tři řádky a byla vytvořena pomocí zásady konsolidace dodávek *CustomerMode*.
- Druhá dodávka, která nepoužívá způsob dopravy *Airways*, byla vytvořena pomocí zásady konsolidace dodávek *CustomerOrderNo*.

### <a name="release-sales-orders-from-order-set-2"></a>Uvolnění prodejních objednávek ze sady objednávek 2

Následujte [základní postup uvolnění do skladu](#release-procedure) a uvolněte prodejní objednávky ze sady objednávek 2.

Po dokončení byste měli vidět, že byly vytvořeny tři dodávky:

- První dodávka obsahuje položky *Hořlavý*.
- Každá ze dvou dalších zásilek obsahuje jeden řádek, který má položku *Explozivní*.

### <a name="release-sales-orders-from-order-set-3"></a>Uvolnění prodejních objednávek ze sady objednávek 3

Následujte [základní postup uvolnění do skladu](#release-procedure) a uvolněte prodejní objednávky ze sady objednávek 3.

Po dokončení byste měli vidět, že došlo k následujícím akcím:

- Byla aktualizována jedna existující dodávka (dodávka, která byla vytvořena při uvolnění sady objednávek 2 do skladu). Byl přidán řádek s položkou *Hořlavý*.
- Byla vytvořena jedna nová dodávka, která obsahuje položku *Explozivní*.

### <a name="release-sales-orders-from-order-set-4"></a>Uvolnění prodejních objednávek ze sady objednávek 4

Následujte [základní postup uvolnění do skladu](#release-procedure) a uvolněte prodejní objednávky ze sady objednávek 4.

Až skončíte, měli byste vidět, že jedna existující dodávka (kde je pole **Žádost zákazníka** nastaveno na *1*) byla aktualizována. Byl k ní přidán jeden nový řádek.

### <a name="release-sales-orders-from-order-set-5"></a>Uvolnění prodejních objednávek ze sady objednávek 5

Následujte [základní postup uvolnění do skladu](#release-procedure) a uvolněte prodejní objednávky ze sady objednávek 5.

Po dokončení byste měli vidět, že došlo k následujícím akcím:

- Jedna existující dodávka (kde je pole **Žádost zákazníka** nastaveno na *1*) byla aktualizována. Řádek z prodejní objednávky 5-3 (kde je pole **Žádost zákazníka** nastaveno na *1*) byl k ní přidán.
- Byla vytvořena jedna nová dodávka, kde řádky z prodejních objednávek 5-1 a 5-2 jsou seskupeny do jedné dodávky.

### <a name="release-sales-orders-from-order-set-6"></a>Uvolnění prodejních objednávek ze sady objednávek 6

Následujte [základní postup uvolnění do skladu](#release-procedure) a uvolněte prodejní objednávky ze sady objednávek 6.

Po dokončení byste měli vidět, že byly vytvořeny čtyři dodávky:

- Řádky ze dvou objednávek pro zákazníka *US-003* byly seskupeny do jedné dodávky pomocí zásady konsolidace dodávek *Fond objednávek*.
- Řádky ze dvou objednávek pro zákazníka *US-004* byly seskupeny do jedné dodávky pomocí zásady konsolidace dodávek *Fond objednávek*.
- Řádky z objednávek 6-5 a 6-6 pro zákazníka *US-007* byly seskupeny do jedné dodávky pomocí zásady konsolidace dodávek *Fond objednávek*.
- Řádky z objednávek 6-7 a 6-8 pro zákazníka *US-007* byly seskupeny do jedné dodávky pomocí zásady konsolidace dodávek *CrossOrder*.

## <a name="additional-resources"></a>Další prostředky

- [Přehled zásad konsolidace dodávek](about-shipment-consolidation-policies.md)
- [Konfigurace zásad konsolidace dodávek](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]