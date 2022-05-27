---
title: Globální parametry mobilního zařízení
description: Toto téma vysvětluje, jak nastavit mobilní zařízení na stránce Parametry řízení skladu.
author: Mirzaab
ms.date: 08/13/2021
ms.topic: article
ms.search.form: WHS
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-13
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 0ae04c86ff1eafb649fcef7c34ace66bdc3e5cb8
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/03/2022
ms.locfileid: "8679158"
---
# <a name="global-mobile-device-parameters"></a>Globální parametry mobilního zařízení

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak nastavit parametry globální správy skladu, které ovlivňují interakci systému s mobilními zařízeními.

Další informace o tom, jak nastavit pracovníky skladu, najdete v článku [Řízení pracovníků skladu](manage-warehouse-workers.md). Další informace týkající se zpracování registračních značek na mobilních zařízeních získáte v tématu [Příjem registrační značky prostřednictvím mobilní aplikace Warehouse Management](warehousing-mobile-device-app-license-plate-receiving.md). Další informace o procesech cyklické inventury najdete v článcích [Cyklická inventura](cycle-counting.md) a [Příkladové scénáře cyklické inventury](cycle-counting-scenarios.md).

## <a name="open-the-warehouse-management-parameters-page"></a>Otevření stránky parametrů řízení skladu

Chcete-li otevřít stránku **Parametry řízení skladu**, přejděte do nabídky **Řízení skladu \> Nastavení \> Parametry řízení skladu**. Poté můžete nastavit pole související s prací na mobilním zařízení, jak je popsáno v další části tohoto tématu.

## <a name="mobile-device-fasttab-on-the-general-tab"></a>Záložka Mobilní zařízení na kartě Obecné

Globální nastavení mobilního zařízení najdete na záložce **Mobilní zařízení** na kartě **Všeobecné** ve stránce **Parametry řízení skladu**. K dispozici jsou následující pole.

| Pole | popis |
|---|---|
| Typ poznámky mobilního zařízení | Vyberte typ informace zobrazené pracovníkům během výdeje prodejních objednávek. |
| Limit skenovaného množství | Zadejte maximální množství položky, které může pracovník během každé relace naskenovat pomocí té položky nabídky mobilního zařízení, jejíž **Proces tvorby práce** má hodnotu *Příchozí úprava*. Toto pole neovlivňuje skenování prováděná pomocí jiného typu položky nabídky. |
| Použít protokolování relace mobilního zařízení | Nastavte tuto možnost na *Ano*, chcete-li uchovávat protokol o historii přihlášení pracovníka. Chcete-li zobrazit protokol, přejděte na **Pracovní relace uživatelů \> Dotazy a zprávy \> Protokoly mobilních zařízení \> Pracovní relace uživatelů**. |
| Počet uložených chyb | Zadejte maximální počet záznamů o chybách, které by měl systém uložit. Chcete-li zobrazit protokol chyb, přejděte na **Pracovní relace uživatelů \> Dotazy a zprávy \> Protokoly mobilních zařízení \> Pracovní relace uživatelů**. |
| Deník převodů výchozího skladu | Vyberte deník, který se používá, když pracovníci používají mobilní zařízení k přesunu produktů z jednoho skladu do druhého. |
| Povolit registraci řádku nákupní objednávky v externí kontrole | Nastavte tuto možnost na *Ano* pokud pracovníci mají být schopni používat mobilní zařízení k registraci řádků objednávek pro nákupní objednávky, které mají **Stav schválení** s hodnotou *Na externí kontrole*. Nastavte tuto možnost na *Ne*, chcete-li zabránit pracovníkům v registraci řádků pro nákupní objednávky, které jsou v externí kontrole. |
| Povolit podporu Nástroje pro vzdálenou správu serveru (RSAT) | Pole aktivuje validátor úloh mobilní aplikace Warehouse Management, který zaznamenává a ověřuje každý krok, který aplikace provede. Protože tento proces může výrazně zpomalit výkon systému, měli byste validátor aktivovat pouze během testování. Nikdy byste jej neměli povolit v produkčním prostředí. |
