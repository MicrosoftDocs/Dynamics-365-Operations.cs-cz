---
title: Přijetí registrační značky prostřednictvím aplikace skladu
description: V tomto tématu je vysvětleno, jak nastavit aplikaci skladu na podporu použití procesu příjmu registračních značek pro příjem fyzických zásob.
author: perlynne
manager: tfehr
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSParameters, WHSRFMenuItem, WHSLicensePlate, WHSPackingStructure
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 0fe02a83d05e4b86694c1b210906128ac0cf6a84
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998421"
---
# <a name="license-plate-receiving-via-the-warehouse-app"></a>Přijetí registrační značky prostřednictvím aplikace skladu

[!include [banner](../includes/banner.md)]

V tomto tématu je vysvětleno, jak nastavit aplikaci skladu, aby podporovala použití procesu příjmu registračních značek pro příjem fyzických zásob.

Pomocí této funkce můžete rychle zaznamenat příjem příchozích zásob, který souvisí s avízem expedice zboží (ASN). Systém při expedici převodního příkazu procesy správy skladu automaticky vytvoří avízo expedice zboží. U procesu nákupní objednávky lze ASN zaznamenat ručně nebo je lze automaticky importovat pomocí procesu příchozí datové entity ASN.

Data ASN jsou spojena s náklady a zásilkami prostřednictvím *struktur balení*, kde palety (nadřazené registrační značky) mohou obsahovat případy (vnořené registrační značky).

> [!NOTE]
> Chcete-li snížit počet skladových transakcí v případě, že jsou použity struktury balení, které mají vnořené registrační značky, systém zaznamená fyzické množství na skladě na nadřízené registrační značce. Chcete-li aktivovat pohyb fyzického množství na skladě z nadřazené registrační značky na základě dat struktury balení, musí mobilní zařízení poskytnout položku nabídky, která je založena na procesu tvorby práce *Zabalit do vnořených registračních značek*.

## <a name="warehousing-mobile-device-app-processing"></a>Zpracování skladových aplikací pro mobilní zařízení

Když pracovník skenuje příchozí ID registrační značky, systém inicializuje proces přijímání registrační značky. Na základě těchto informací se obsah registrační značky (data pocházející z ASN) fyzicky zaregistruje v místě příchozího doku. Následné toky budou záviset na potřebách vašeho obchodního procesu.

## <a name="work-policies"></a>Zásady práce

Stejně jako (například) proces položky mobilního zařízení *Nahlásit jako dokončené* podporuje i proces přijímání registrační značky několik pracovních postupů na základě definovaného nastavení.

### <a name="work-policies-with-work-creation"></a>Pracovní zásady s vytvářením práce

Když zaregistrujete příchozí položky pomocí pracovních zásad, které vytvářejí práci, systém generuje a ukládá odložené pracovní záznamy pro každou registraci. Pokud používáte pracovní proces *přijímání a odkládání registrační značky*, jsou registrace a odkládání zpracovány jako jediná operace pomocí jediné položky nabídky mobilního zařízení. Pokud používáte proces *Příjem poznávací značky*, pak jsou procesy přijímání a odkládání zpracovávány jako dvě různé skladové operace, každá s vlastní položkou nabídky mobilního zařízení.

### <a name="work-policies-without-work-creation"></a>Pracovní zásady bez vytváření práce

Můžete přijímat registrační značku bez vytváření práce. Pokud definujete pracovní zásady, které mají typ pracovního příkazu *Doklad o převodu* a/nebo *Nákupní objednávky* a tento proces použijete pro *Příjem (a odložení) registrační značky*, následující dva procesy mobilní aplikace Warehousing nebudou fungovat. Místo toho pouze zaregistrují příchozí fyzické zásoby v registrační značce v příchozím přijímajícím doku.

- *Přijetí registrační značky*
- *Přijetí a odložení registrační značky*

> [!NOTE]
> - Musíte definovat alespoň jedno umístění pro pracovní zásady v části **Místo zásob**. Nemůžete zadat stejné umístění pro více pracovních zásad.
> - Možnost **Tisk štítku** pro mobilní zařízení s aplikací Warehousing nevytisknou štítek registrační značky bez vytvoření práce.

Abyste tuto funkci zpřístupnili ve svém systému, musíte zapnout funkci *Vylepšení příjmu registrační značky* v okně [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="receive-inventory-on-a-location-that-doesnt-track-license-plates"></a>Příjem zásob na místě, které nesleduje registrační značky

Je možné použít umístění skladu, které je přiřazeno k profilu místa, i když není volba **Použít sledování registrační značky** zapnutá. Proto, když obdržíte zásoby, můžete přímo zaregistrovat zásoby na skladě bez vytvoření práce.

## <a name="add-mobile-device-menu-items-for-each-receiving-location-in-a-warehouse"></a>Přidejte položky nabídky mobilního zařízení pro každé přijímací místo ve skladu

Funkce *Vylepšení příjmu registrační značky* umožňuje příjem na jakémkoli místě ve skladu přidáním položek nabídky registrační značky (a odložení) do mobilní aplikace Warehousing. Dříve systém podporoval příjem pouze ve výchozím umístění, které je definováno pro každý sklad. Když je však tato funkce zapnutá, položky nabídky mobilního zařízení pro příjem (a odložení) registrační značky nyní poskytují volbu **Použít výchozí data**, která vám umožní vybrat vlastní umístění „do“ pro každou položku nabídky. (Tato možnost již byla k dispozici pro některé jiné typy položek nabídky.)

Abyste tuto funkci zpřístupnili ve svém systému, musíte zapnout funkci *Vylepšení příjmu registrační značky* v okně [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="show-or-skip-the-receiving-summary-page"></a>Zobrazit nebo přeskočit stránku Souhrn přijetí

Můžete použít funkci *Určit, zda zobrazit stránku souhn upříjmu na mobilních zařízeních*, chcete-li využít další detailní tok aplikací Warehouse v rámci procesu získávání registrační značky.

Je-li tato funkce zapnuta, položky nabídky mobilního zařízení pro příjem registračních značek nebo příjem a zaskladnění registračních značek poskytnou nastavení **Zobrazit stránku souhnu příjmu**. Toto nastavení má následující možnosti:

- **Zobrazit podrobný souhrn** – během příjmu registrační značky se zaměstnanci zobrazí další stránka s úplnými informacemi o ASN.
- **Přeskočit souhrn** – pracovníci nebudou moci zobrazit úplné informace o ASN. Pracovníci skladu také nebudou moci v průběhu procesu příjmu nastavovat dispoziční kód ani přidávat výjimky.

Abyste tuto funkci zpřístupnili ve svém systému, musíte zapnout funkci *Určete, zda se má zobrazit souhrnná stránka příjmu na mobilních zařízeních* v okně [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a>Zabránit použití převodním příkazem expedovaných registračních značek v jiných skladech než je cílový Sklad

Proces příjmu registrační značky je možné použít v případě, že ASN obsahuje ID registrační značky, které již existuje, a má fyzická data na skladě v jiném skladovém místě, než je skladové místo, kde dochází k registraci registrační značky.

Pro scénáře převodního příkazu, u nichž tranzitní sklad nesleduje registrační značky (a proto nesleduje fyzické zásoby na skladě na registrační značku), můžete pomocí funkce *Zabránit použití převodním příkazem expedovaných registračních značek v jiných skladech než je cílový sklad*, aby se zabránilo fyzické aktualizaci množství na skladě u registračních značek, které jsou v tranzitu.

Abyste tuto funkci zpřístupnili ve svém systému, musíte zapnout funkci *Zabraňte tomu, aby byly registrační značky dodané v příkazu převodu použity v jiných skladech než v cílovém skladu* v okně [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Chcete-li spravovat funkce, když je tato funkce dostupná, postupujte podle následujících kroků.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Parametry řízení skladu**.
1. Na kartě **Obecné**, na pevné záložce **Registrační značky** nastavte pole **Zásady tranzitu registračních značek skladu** na jednu z následujících hodnot:

    - **Povolit opakované použití nesledované registrační značky** - systém pracuje stejným způsobem, když není k dispozici funkce *Zabránit použití převodním příkazem expedovaných registračních značek v jiných skladech než je cílový sklad*. Tato hodnota je výchozím nastavením při prvním zapnutí funkce.
    - **Zabránit opakovanému použití nesledované registrační značky** – budou povoleny pouze aktualizace množství na skladě, které souvisí s odeslanou registrační značkou v cílovém skladě, dokud nebude přijat převodní příkaz.

## <a name="more-information"></a>Další informace

Další informace o položkách nabídky mobilního zařízení naleznete v tématu [Nastavení mobilních zařízení pro práci ve skladu](configure-mobile-devices-warehouse.md).

Více informací o scénáři výroby *Nahlásit jako hotovo* získáte v tématu [Přehled pracovních zásad skladu](warehouse-work-policies.md).

Další informace o správě příchozího vytížení získáte v části [Skladová manipulace s příchozím zatížením pro nákupní objednávky](inbound-load-handling.md).
