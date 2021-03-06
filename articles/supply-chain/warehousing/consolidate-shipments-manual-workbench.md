---
title: Konsolidace dodávek pomocí pracovní plochy dodávek zásilek
description: Toto téma představuje scénář, ve kterém je více objednávek uvolněno do skladu a později konsolidováno do dodávek pomocí pracovní plochy konsolidace dodávek.
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSShipConsolidationSetShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 29dd403ce2378beb6f4ba71a0b3c0836eed7566a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838411"
---
# <a name="consolidate-shipments-by-using-the-shipment-consolidation-workbench"></a>Konsolidace dodávek pomocí pracovní plochy dodávek zásilek

[!include [banner](../includes/banner.md)]

Toto téma představuje scénář, ve kterém je více objednávek uvolněno do skladu a později konsolidováno do dodávek pomocí pracovní plochy konsolidace dodávek.

## <a name="make-demo-data-available"></a>Zpřístupnění ukázkových dat

Scénář v tomto tématu odkazuje na hodnoty a záznamy, které jsou součástí standardních ukázkových dat poskytovaných pro aplikaci Microsoft Dynamics 365 Supply Chain Management. Pokud chcete při cvičení použít hodnoty, které jsou zde uvedeny, nezapomeňte pracovat v prostředí, ve kterém jsou nainstalovaná ukázková data, a nastavte právnickou osobu na **USMF**, než začnete.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Nastavení zásad konsolidace dodávek a filtry produktů

Scénář, který je zde popsán, předpokládá, že jste již tuto funkci zapnuli a provedli cvičení v [konfiguraci zásad konsolidace dodávek](configure-shipment-consolidation-policies.md) a vytvořili zásady a další záznamy, které jsou zde popsány. Než budete pokračovat v tomto scénáři, nezapomeňte tato cvičení provést.

## <a name="turn-on-the-manual-shipment-consolidation-feature"></a>Zapnutí funkce rušní konsolidace dodávek

Než budete moci používat funkci *Ruční konsolidace dodávek*, musíte ji zapnout ve svém systému. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Ruční konsolidace dodávek*

Jak bylo uvedeno v [zásadách konfigurace konsolidace dodávek](configure-shipment-consolidation-policies.md), musíte také zapnout funkci *Konsolidovat dodávku* před vytvořením zásad. Tento krok byste však již měli dokončit.

## <a name="create-the-sales-orders-for-this-scenario"></a>Vytvoření prodejních objednávek pro tento scénář

Začněte vytvořením kolekce prodejních objednávek, se kterou můžete pracovat. Musíte pracovat se skladem, který je povolen pro rozšířené procesy skladu (WMS). Pokud není výslovně uveden jiný sklad, musí být stejný sklad použit pro každou z následujících sad objednávek.

Přejděte na **Pohledávky \> Objednávky \> Všechny prodejní objednávky** a vytvořte kolekci prodejních objednávek, jejichž nastavení jsou popsána v následujících pododdílech.

### <a name="create-order-set-1"></a>Vytvoření sady objednávek 1

#### <a name="sales-orders-1-1-and-1-2"></a>Prodejní objednávky 1-1 a 1-2

1. Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:

    - **Účet zákazníka:** *US-001*
    - **Způsob doručení:** *Airwa-Air*

1. Přidejte řádek objednávky, který má následující nastavení:

    - **Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)
    - **Množství:** *1.00*

1. Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.

#### <a name="sales-order-1-3"></a>Prodejní objednávka 1-3

1. Vytvořte prodejní objednávku, která má následující nastavení:

    - **Účet zákazníka:** *US-001*
    - **Způsob dodání:** *10*

1. Přidejte řádek objednávky, který má následující nastavení:

    - **Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)
    - **Množství:** *1.00*

1. Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.
1. Přidejte druhý řádek objednávky, který má následující nastavení:

    - **Číslo položky:** *A0002* (položka, ke které není přiřazen filtr **Kód 4**)
    - **Množství:** *1.00*
    - **Způsob doručení:** *Airwa-Air*

1. Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci druhého řádku objednávky.

### <a name="create-order-set-2"></a>Vytvoření sady objednávek 2

#### <a name="sales-orders-2-1-and-2-2"></a>Prodejní objednávky 2-1 a 2-2

1. Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:

    - **Účet zákazníka:** *US-002*
    - **Způsob doručení:** *Airwa-Air*

1. Přidejte řádek objednávky, který má následující nastavení:

    - **Číslo položky:** *M9200* (položka, kde je filtr **Kód 4** nastaven na *Hořlavý*)
    - **Množství:** *1.00*

1. Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.
1. Přidejte druhý řádek objednávky, který má následující nastavení:

    - **Číslo položky:** *M9201* (položka, kde je filtr **Kód 4** nastaven na *Explozivní*)
    - **Množství:** *1.00*
    - **Způsob doručení:** *Airwa-Air*

1. Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci druhého řádku objednávky.

### <a name="create-order-set-3"></a>Vytvoření sady objednávek 3

#### <a name="sales-orders-3-1-and-3-2"></a>Prodejní objednávky 3-1 a 3-2

1. Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:

    - **Účet zákazníka:** *US-001*
    - **Žádost zákazníka:** *1*

1. Přidejte řádek objednávky, který má následující nastavení:

    - **Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)
    - **Množství:** *1.00*

1. Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.

#### <a name="sales-orders-3-3-and-3-4"></a>Prodejní objednávky 3-3 a 3-4

1. Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:

    - **Účet zákazníka:** *US-001*
    - **Žádost zákazníka:** *2*

1. Přidejte řádek objednávky, který má následující nastavení:

    - **Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)
    - **Množství:** *1.00*

1. Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.

### <a name="create-order-set-4"></a>Vytvoření sady objednávek 4

#### <a name="sales-orders-4-1-and-4-2"></a>Prodejní objednávky 4-1 a 4-2

1. Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:

    - **Účet zákazníka:** *US-003*

1. Přidejte řádek objednávky, který má následující nastavení:

    - **Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)
    - **Množství:** *1.00*

1. Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.

#### <a name="sales-orders-4-3-and-4-4"></a>Prodejní objednávky 4-3 a 4-4

1. Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:

    - **Účet zákazníka:** *US-004*

1. Přidejte řádek objednávky, který má následující nastavení:

    - **Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)
    - **Množství:** *1.00*

1. Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.

#### <a name="sales-orders-4-5-and-4-6"></a>Prodejní objednávky 4-5 a 4-6

1. Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:

    - **Účet zákazníka:** *US-007*
    - **Lokalita:** *6*
    - **Sklad:** *61*
    - **Fond:** *ShipCons*

1. Přidejte řádek objednávky, který má následující nastavení:

    - **Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)
    - **Množství:** *1.00*

1. Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.

#### <a name="sales-orders-4-7-and-4-8"></a>Prodejní objednávky 4-7 a 4-8

1. Vytvořte dvě stejné prodejní objednávky, které mají následující nastavení:

    - **Účet zákazníka:** *US-007*
    - **Lokalita:** *6*
    - **Sklad:** *61*
    - **Fond:** Pole ponechejte prázdné.

1. Přidejte řádek objednávky, který má následující nastavení:

    - **Číslo položky:** *A0001* (položka, ke které není přiřazen filtr **Kód 4**)
    - **Množství:** *1.00*

1. Vyberte **Zásoby \> Rezervace** a poté v podokně akcí vyberte **Rezervovat šarži** pro rezervaci řádku objednávky.

## <a name="release-the-orders-to-the-warehouse"></a>Uvolnění objednávek do skladu

Chcete-li uvolnit každou prodejní objednávku, kterou jste vytvořili pro tento scénář, do skladu, postupujte takto.

1. Přejděte na **Pohledávky \> Objednávky \> Všechny prodejní objednávky**.
1. Vyhledejte a vyberte prodejní objednávku, kterou chcete uvolnit.
1. V podokně akcí na kartě **Sklad** vyberte **Akce \> Uvolnit do skladu** pro uvolnění vybrané prodejní objednávky.
1. Tento postup opakujte pro každou další prodejní objednávku, kterou jste vytvořili pro tento scénář.

## <a name="consolidate-the-shipments-by-using-the-shipment-consolidation-workbench"></a>Konsolidace dodávek pomocí pracovní plochy konsolidace dodávek

1. Přejděte na **Řízení skladu \> Uvolnění do skladu \> Pracovní plocha konsolidace dodávek**.
1. V podokně akcí vyberte **Upravit dotaz**.
1. V dialogovém okně editoru dotazů na kartě **Rozsah** vyberte **Přidat** a přidejte do mřížky řádek, který má následující nastavení:

    - **Tabulka:** *Prodejní objednávky*
    - **Pole:** *Prodejní objednávka*
    - **Kritéria:** Zadejte čárkami oddělený seznam čísel prodejních objednávek pro každou sadu objednávek, kterou jste vytvořili pro tento scénář.

1. Vyberte **OK**, uložte svůj dotaz a zavřete dialogové okno.
1. V podokně akcí klikněte na možnost **Konsolidovat dodávky**.
1. Vyberte všechny dodávky a poté vyberte v podokně akcí možnost **Konsolidovat**.

## <a name="verify-the-shipments"></a>Ověření dodávek

Následující postup umožňuje ověřit dodávky, které byly vytvořeny nebo aktualizovány v důsledku konsolidace dodávky. Použijte ho ke kontrole každé sady objednávek, kterou jste vytvořili pro tento scénář, a poté zkontrolujte následující pododdíly, abyste se ujistili, že jste dosáhli očekávaných výsledků.

1. Přejděte na **Řízení skladu \> Dodávky \> Všechny dodávky**.
1. Najděte a vyberte požadovanou dodávku.
1. Pokud byla při vytváření nebo aktualizaci dodávky použita zásada konsolidace, měli byste ji vidět v poli **Zásada konsolidace dodávek**.

### <a name="related-shipments-for-order-set-1"></a>Související dodávky pro sadu objednávek 1

Měly být vytvořeny dvě dodávky:

- První dodávka obsahuje tři řádky a byla vytvořena pomocí zásady konsolidace dodávek *CustomerMode*.
- Druhá dodávka, která nepoužívá způsob dopravy *Airways*, byla vytvořena pomocí zásady konsolidace dodávek *CustomerOrderNo*.

### <a name="related-shipments-for-order-set-2"></a>Související dodávky pro sadu objednávek 2

Měly být vytvořeny tři dodávky:

- První dodávka obsahuje položky *Hořlavý*.
- Každá ze dvou dalších zásilek obsahuje jeden řádek, který má položku *Explozivní*.

### <a name="related-shipments-for-order-set-3"></a>Související dodávky pro sadu objednávek 3

Měly být vytvořeny dvě dodávky:

- První dodávka obsahuje řádky objednávky z prodejní objednávky, kde je pole **Žádost zákazníka** nastaveno na *1*.
- Druhá dodávka obsahuje řádky objednávky z prodejní objednávky, kde je pole **Žádost zákazníka** nastaveno na *2*.

### <a name="related-shipments-for-order-set-4"></a>Související dodávky pro sadu objednávek 4

Měly být vytvořeny čtyři dodávky:

- Řádky ze dvou objednávek pro zákazníka *US-003* byly seskupeny do jedné dodávky pomocí zásady konsolidace dodávek *Fond objednávek*.
- Řádky ze dvou objednávek pro zákazníka *US-004* byly seskupeny do jedné dodávky pomocí zásady konsolidace dodávek *Fond objednávek*.
- Řádky z objednávek 4-5 a 4-6 pro zákazníka *US-007* byly seskupeny do jedné dodávky pomocí zásady konsolidace dodávek *Fond objednávek*.
- Řádky z objednávek 4-7 a 4-8 pro zákazníka *US-007* byly seskupeny do jedné dodávky pomocí zásady konsolidace dodávek *CrossOrder*.

## <a name="additional-resources"></a>Další prostředky

- [Zásady konsolidace dodávek](about-shipment-consolidation-policies.md)
- [Konfigurace zásad konsolidace dodávek](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]