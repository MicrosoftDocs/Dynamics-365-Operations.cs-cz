---
title: Připraveno k platbě
description: Toto téma ukazuje, jak označit zaměstnance jako připraveného k výplatě v Dynamics 365 Human Resources.
author: marcelbf
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 80bba5446eb7a87d96a7da4ae856cb5ca114ce52
ms.sourcegitcommit: 24e20b3b96834b23311f1bf5dbab28baf3323728
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/08/2021
ms.locfileid: "7483775"
---
# <a name="ready-to-pay"></a>Připraveno k platbě

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

> [!NOTE]
> Pokud chcete označit zaměstnance jako připraveného k výplatě, musíte nejprve povolit funkci **(Náhled) integrace mezd** ve správě funkcí. Další informace o povolení funkcí Preview naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).

Tato funkce umožňuje odborníkům v oblasti lidských zdrojů pochopit, kteří zaměstnanci jsou připraveni na zpracování mezd a kteří vyžadují akci, než je spotřebuje externí poskytovatel mezd.

## <a name="mark-employee-as-ready-to-pay"></a>Označit zaměstnance jako připraveného k platbě

Shromažďování a ověřování informací o zaměstnancích může být časově náročné a náchylné k chybám. Poskytnutím způsobu, jak mohou odborníci na lidské zdroje kontrolovat a snadno aktualizovat informace o zaměstnancích, Dynamics 365 Human Resources pomáhá zkrátit čas strávený přípravou na zpracování mezd.

Onačení zaměstnance jako připraveného k výplatě:

1. Otevřete **Správu kompenzací**. V pracovním prostoru jsou dvě dlaždice: 
    - **Zaměstnanci, kteří jsou připraveni pro výplatu**
    - **Zaměstnanci nejsou připraveni k výplatě**
    ![Pracovní prostor pro správu kompenzací.](./media/hr-ready-to-pay-1-workspace.png)

2. Vyberte dlaždici **Zaměstnanci nejsou připraveni v výplatě**.

3. Vyberte zaměstnance, kteří mají být ověřeni. Na **Kartě Mzdy** ve skupině **Připraveno k výplatě** vyberte **Ověřit**.
    ![Ověit zaměstnance.](./media/hr-ready-to-pay-2-validate.png)

4. Chcete-li zkontrolovat výsledky, na **Kartě Mzdy** ve skupině **Připraveno k výplatě** vyberte **Výsledky**.

## <a name="validation"></a>Ověření

Před označením zaměstnance jako připraveného k platbě bude ověřena úplnost profilu zaměstnance.

![Ověření výsledků.](./media/hr-ready-to-pay-3-results.png)

| Ověření | Podrobnosti |
| --- | --- |
| **Parametr účelu adresy** | Potvrdí, zda je parametr **Použijte účel výplatní adresy** vybrán. |
| **Adresa mzdy** | Potvrdí, zda má profil pracovníka alespoň jednu adresu s účelem **Místo bydliště** nebo **Místo práce mzdy**, a pro každý účel existuje pouze jedna adresa. |
| **Zaměstnání** | Potvrdí, zda má pracovník alespoň jedno zaměstnání (současné, předchozí nebo budoucí). |
| **Identifikační číslo** | Potvrdí, zda je parametr **Použít typy identifikace při zpracování mezd** na stránce **Parametry lidských zdrojů** nastaven na **Ano** a zda je typ identifikace uvedený v parametru vyplněn v pracovním profilu. |
| **Jméno a příjmení** | Potvrzuje vyplnění polí **Jméno** a **Příjmení**.|
| **Pracovní pozice** | Potvrdí, že má pracovník přiřazenou pozici. |
| **Datum narození** | Potvrdí vyplnění pole **Narozeniny**. |
| **Kompenzace** | Potvrdí, že je pracovník zapsán do plánu pevné kompenzace. |

Pokud jedno z těchto ověření selže, nemůžete zaměstnance označit jako připraveného k platbě.

Pokud je pole **Připraveno k výplatě** nastaveno na **Ne**, je to indikace, že musíte provést akci, abyste se ujistili, že je profil pracovníka kompletní. To nezastaví data, která mají být vystavena v jakékoli datové entitě. 

## <a name="known-issues"></a>Známé problémy

- Musíte deaktivovat funkci **Efektivnější vstup zaměstnanců** ve správě funkcí. Pokud použijete tuto funkci, dlaždice v pracovním prostoru správy kompenzací nebudou fungovat správně.
- Na stránce **Pracovník** na kartě **Mzdy** je skupina **Připraveno k výplatě** k dispozici jakékoli uživatelské roli. 

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API integrace mezd](hr-admin-integration-payroll-api-introduction.md)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
