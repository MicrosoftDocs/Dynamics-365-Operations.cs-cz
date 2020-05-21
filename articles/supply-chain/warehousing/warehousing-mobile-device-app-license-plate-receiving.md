---
title: Přijetí registrační značky prostřednictvím aplikace warehousing
description: V tomto tématu je vysvětleno, jak nastavit aplikaci skladu na podporu použití procesu příjmu registračních značek pro příjem fyzických zásob.
author: perlynne
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 7d5ac6598ab80ece0164d7c92f5d84e91d21b385
ms.sourcegitcommit: ffd845d4230646499b6f074cb43e69ab95787671
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2020
ms.locfileid: "3346369"
---
# <a name="license-plate-receiving-via-the-warehousing-app"></a>Přijetí registrační značky prostřednictvím aplikace warehousing

V tomto tématu je vysvětleno, jak nastavit aplikaci skladu, aby podporovala použití procesu příjmu registračních značek pro příjem fyzických zásob.

Pomocí této funkce můžete rychle zaznamenat příjem příchozích zásob, který souvisí s avízem expedice zboží (ASN). Systém při expedici převodního příkazu procesy správy skladu automaticky vytvoří avízo expedice zboží. U procesu nákupní objednávky lze ASN zaznamenat ručně nebo je lze automaticky importovat pomocí procesu příchozí datové entity ASN.

Data ASN jsou spojena s náklady a zásilkami prostřednictvím *struktur balení*, kde palety (nadřazené registrační značky) mohou obsahovat případy (vnořené registrační značky).

> [!NOTE]
> Chcete-li snížit počet skladových transakcí v případě, že jsou použity struktury balení, které mají vnořené registrační značky, systém zaznamená fyzické množství na skladě na nadřízené registrační značce. Chcete-li aktivovat pohyb fyzického množství na skladě z nadřazené registrační značky na základě dat struktury balení, musí mobilní zařízení poskytnout položku nabídky, která je založena na procesu tvorby práce *Zabalit do vnořených registračních značek*.

<!-- To be used later (will require further editing):
## Warehousing mobile device app processing

When a worker scans an incoming license plate ID, the system initializes a license plate receiving process. Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location. The flows that follow will depend your business process needs.

## Work policies

As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.

### Work policies with work creation

Registration of physical on-hand where either the same warehouse worker immediately process a put-away work process following the inbound receiving (License plate receiving and put away) or where the registration and put away process gets handled as two different warehouse operations (License plate receiving) following the processing of the put-away work by using the existing work process via another mobile device menu item.

## Work policies without work creation

You can use the license plate receiving process without creating work by using the *License plate receiving without creating work* feature.

By defining **Work policies** with a **Work order type** of *Transfer receipt* and/or *Purchase orders*, and using the **Process** for **License plate receiving (and put away)**, the two Warehousing app process:

- License plate receiving
- License plate receiving and put away

will not create work, but only register the inbound physical inventory on the license plate at the inbound receiving dock.

For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).

-->

## <a name="show-or-skip-the-receiving-summary-page"></a>Zobrazit nebo přeskočit stránku Souhrn přijetí

Můžete použít funkci *Určit, zda zobrazit stránku souhrnu příjmu na mobilních zařízeních*, chcete-li využít další detailní tok aplikací Warehousing v rámci procesu získávání registrační značky.

Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Určit, zda zobrazit stránku souhn upříjmu na mobilních zařízeních*

Je-li tato funkce zapnuta, položky nabídky mobilního zařízení pro příjem registračních značek nebo příjem a zaskladnění registračních značek poskytnou nastavení **Zobrazit stránku souhnu příjmu**. Toto nastavení má následující možnosti:

- **Zobrazit podrobný souhrn** – během příjmu registrační značky se zaměstnanci zobrazí další stránka s úplnými informacemi o ASN.
- **Přeskočit souhrn** – pracovníci nebudou moci zobrazit úplné informace o ASN. Pracovníci skladu také nebudou moci v průběhu procesu příjmu nastavovat dispoziční kód ani přidávat výjimky.

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a>Zabránit použití převodním příkazem expedovaných registračních značek v jiných skladech než je cílový Sklad

Proces příjmu registrační značky je možné použít v případě, že ASN obsahuje ID registrační značky, které již existuje, a má fyzická data na skladě v jiném skladovém místě, než je skladové místo, kde se registrují registrační značky.

Pro scénáře převodního příkazu, u nichž tranzitní sklad nesleduje registrační značky (a proto nesleduje fyzické zásoby na skladě na registrační značku), můžete pomocí funkce *Zabránit použití převodním příkazem expedovaných registračních značek v jiných skladech než je cílový sklad*, aby se zabránilo fyzické aktualizaci množství na skladě u registračních značek, které jsou v tranzitu.

Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Řízení skladu*
- **Název funkcee:** *Zabránit použití převodním příkazem expedovaných registračních značek v jiných skladech než je cílový sklad*

Chcete-li spravovat funkce, když je tato funkce dostupná, postupujte podle následujících kroků.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Parametry řízení skladu**.
1. Na kartě **Obecné**, na pevné záložce **Registrační značky** nastavte pole **Zásady tranzitu registračních značek skladu** na jednu z následujících hodnot:

    - **Povolit opakované použití nesledované registrační značky** - systém pracuje stejným způsobem, když není k dispozici funkce *Zabránit použití převodním příkazem expedovaných registračních značek v jiných skladech než je cílový sklad*. Tato hodnota je výchozím nastavením při prvním zapnutí funkce.
    - **Zabránit opakovanému použití nesledované registrační značky** – budou povoleny pouze aktualizace množství na skladě, které souvisí s odeslanou registrační značkou v cílovém skladě, dokud nebude přijat převodní příkaz.

## <a name="more-information"></a>Další informace

<!-- To read more about inbound loads, see [Link for Inbound load (Olga's doc.)] -->

Další informace o položkách nabídky mobilního zařízení naleznete v tématu [Nastavení mobilních zařízení pro práci ve skladu](configure-mobile-devices-warehouse.md).
