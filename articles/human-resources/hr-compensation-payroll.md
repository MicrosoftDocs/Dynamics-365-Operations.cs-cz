---
title: Připraveno k platbě
description: Toto téma ukazuje, jak označit zaměstnance jako připraveného k výplatě v Dynamics 365 Human Resources.
author: marcelbf
ms.date: 07/13/2020
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
ms.openlocfilehash: 70b3f31db459fe021caf08fe09b2e44a597294d1992ee16a69efd8745941a4bd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732410"
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

1. Otevřete **Správu kompenzací**. V pracovním prostoru jsou dvě dlaždice 
    - **Zaměstnanci, kteří jsou připraveni pro výplatu**
    - **Zaměstnanci nejsou připraveni k výplatě**
    ![Pracovní prostor pro správu kompenzací.](./media/hr-ready-to-pay-1-workspace.png)

2. Vyberte dlaždici **Zaměstnanci nejsou připraveni v výplatě**.

3. Vyberte zaměstnance, kteří mají být ověřeni. Na **Kartě Mzdy** ve skupině **Připraveno k výplatě** vyberte **Ověřit**.
    ![Ověit zaměstnance.](./media/hr-ready-to-pay-2-validate.png)

4. Chcete-li zkontrolovat výsledky, na **Kartě Mzdy** ve skupině **Připraveno k výplatě** vyberte **Výsledky**.

## <a name="validation"></a>Ověření

Před označením zaměstnance jako připraveného k platbě provede systém základní ověření úplnosti profilu.

![Ověření výsledků.](./media/hr-ready-to-pay-3-results.png)

Následující tabulka uvádí více informací o všech provedených ověřeních. 

| Ověření | Podrobnosti |
| --- | --- |
| Parametr účelu adresy | Ověřuje, zda je parametr **Použijte účel výplatní adresy** je zapnutý. |
| Adresa mzdy | Ověřuje, zda má profil pracovníka alespoň jednu adresu s účelem „Místo bydliště“ nebo „Místo práce mzdy“, a pro každý účel existuje pouze jedna adresa. |
| Zaměstnání | Ověřte, zda má pracovník alespoň jedno zaměstnání (současné, předchozí nebo budoucí). |
| Identifikační číslo | Ověřuje, zda je parametr „Použít typy identifikace při zpracování mezd“ nastaven na ano a zda je typ identifikace uvedený v parametru vyplněn v pracovním profilu. |
| Jméno a příjmení | Ověřuje, zda je profil pracovníka platný, a kontroluje, zda jsou pole **Jméno** a **Příjmení** vyplněny.|
| Pracovní pozice | Ověřte, zda má pracovník přiřazenou pozici. |
| Datum narození | Ověřuje, zda je profil pracovníka platný, a kontroluje, zda je vyplněno pole **Narozeniny**. |
| Kompenzace | Ověřte, zda je pracovník zapsán do plánu pevné kompenzace. |

Pokud jedno z těchto ověření selže, nemůžete zaměstnance označit jako připraveného k platbě.

Pokud je pole **Připraveno k výplatě** nastaveno na **Ne**, je to indikace, že musíte provést akci, abyste se ujistili, že je profil pracovníka kompletní. To nezastaví data, která mají být vystavena v jakékoli datové entitě. 

## <a name="known-issues"></a>Známé problémy

- Musíte deaktivovat funkci **Efektivnější vstup zaměstnanců** ve správě funkcí. Pokud použijete tuto funkci, dlaždice v pracovním prostoru správy kompenzací nebudou fungovat správně.
- Ve formuláři pracovníka **Karta Mzdy** je skupina **Připraveno k výplatě** k dispozici jakékoli uživatelské roli. 

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API integrace mezd](hr-admin-integration-payroll-api-introduction.md)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
