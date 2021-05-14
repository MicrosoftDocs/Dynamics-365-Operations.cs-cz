---
title: Řešení potíží s příchozími skladovými operacemi
description: Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s příchozími skladovými operacemi v Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6f6d689c596b4ec924cb50ec3bea8ce907e6dc6b
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920980"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a>Řešení potíží s příchozími skladovými operacemi

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s příchozími skladovými operacemi v Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a>Zobrazuje se následující chybová zpráva: „Objednávka kvality %1 byla vygenerována. Profil seskupení nebyl nalezen. Zkontrolujte svou konfiguraci."

### <a name="issue-description"></a>Popis problému

Tato chybová zpráva souvisí s přijímacím procesem, kde je zapnutá správa kvality (QMS). V závislosti na konfiguracích ve vašem prostředí mohou problém vyřešit další podrobnosti o transakci, která generuje chybovou zprávu.

### <a name="issue-resolution"></a>Řešení problému

Nejprve zkontrolujte nastavení [výdeje v seskupení](set-up-cluster-picking.md) a ujistěte se, že jsou vaše profily seskupení nastaveny správně. Položku nabídky mobilního zařízení nemůžete použít pro výběr seskupení, pokud nejsou nastaveny profily seskupení. V závislosti na vašem prostředí budete možná muset zkontrolovat další související konfigurace.

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a>Přijímání smíšených registračních značek nefunguje pro žádný dispoziční kód kromě kreditu.

### <a name="issue-description"></a>Popis problému

Když je pole **Akce** pro kód dispozice je nastaveno na *Kredit* nebo *Odpad*, můžete použít pouze položku nabídky [Přijetí smíšené registrační značky](mixed-license-plate-receiving.md) ke zpracování vrácených položek.

### <a name="issue-resolution"></a>Řešení problému

Společnost Microsoft vyhodnotila tento problém a zjistila, že jde o omezení funkcí. V současné době jsou pro příjem smíšených registračních značek podporovány pouze [dispoziční kódy](../service-management/set-up-disposition-codes.md), kde je pole **Akce** nastaveno na *Kredit* nebo *Odpad*.

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a>Když spustím pravidelnou úlohu Aktualizovat potvrzení o přijetí produktu, potvrdí se nepotvrzené nákupní objednávky.

### <a name="issue-description"></a>Popis problému

Po spuštění periodického úkolu *Aktualizovat příjemky produktů* systém automaticky potvrzuje nepotvrzené nákupní objednávky, které mají stav transakce zásob *Registrovaný*.

### <a name="issue-resolution"></a>Řešení problému

Nová funkce zpracování příchozího nákladu *Příjem většího množství nákladu* opravuje tento problém. Chcete-li tuto funkci zapnout, přejděte k pracovnímu prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zapněte následující funkce (v pořadí, v jakém jsou uvedeny):

1. Přiřadit transakce zásob nákupní objednávky k vytížení
1. Nadměrné přijetí množství vytížení

Další informace viz [Zaúčtujte registrované množství produktu oproti nákupním objednávkám](inbound-load-handling.md#post-registered-quantities).

## <a name="when-i-register-inbound-orders-i-receive-the-following-error-message-the-quantity-is-not-valid"></a>Když zaregistruji příchozí objednávky, zobrazí se následující chybová zpráva: „Množství není platné“.

### <a name="issue-description"></a>Popis problému

Pokud je pole **Zásady seskupování registračních značek** nastaveno na *Definováno uživatelem* pro položku nabídky mobilního zařízení, která je použita k registraci příchozích objednávek, zobrazí se chybová zpráva („Množství není platné“) a registraci nelze dokončit.

### <a name="issue-cause"></a>Příčina problému

Když je *Definováno uživatelem* použito jako zásada pro seskupování registračních značek, systém rozdělí příchozí zásoby na samostatné registrační značky, jak udává skupina klasifikace jednotek. Pokud se ke sledování přijímané položky použije číslo dávky nebo sériové číslo, je třeba zadat množství každé dávky nebo série pro každou registrační značku, která je registrována. Pokud množství, které je zadáno pro registrační značku, překročí množství, které ještě musí být přijato pro aktuální dimenze, zobrazí se chybová zpráva.

### <a name="issue-resolution"></a>Řešení problému

Když zaregistrujete položku pomocí položky nabídky mobilního zařízení, kde je pole **Zásady seskupování registračních značek** nastaveno na *Definováno uživatelem*, může systém vyžadovat potvrzení nebo zadání čísel registračních značek, čísel dávek nebo sériových čísel.

Na potvrzovací stránce registrační značky systém zobrazí množství, které je přiděleno pro aktuální registrační značku. Na potvrzovací stránce dávky nebo série systém zobrazí množství, které ještě musí být přijato pro aktuální registrační značku. Bude také obsahovat pole, kde můžete zadat množství, které bude registrováno pro tuto kombinaci registrační značky a čísla dávky nebo sériového čísla. V takovém případě se ujistěte, že množství, které je registrováno pro registrační značku, nepřekročí množství, které ještě musí být přijato.

Případně pokud se při registraci příchozí objednávky vygeneruje příliš mnoho registračních značek, hodnotu pole **Zásady seskupování registračních značek** lze změnit na *Seskupení registračních značek*, položce lze přiřadit novou skupinu klasifikace jednotek nebo možnost **Seskupení registračních značek** pro skupinu klasifikace jednotek může být deaktivována.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
