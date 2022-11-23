---
title: Omezení přístupu k pracovníkům podle právnické osoby
description: Tento článek vysvětluje, jak nastavit přístup pracovníků podle právnické osoby.
author: twheeloc
ms.date: 11/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fadd2c34d31bbd259255596c06a8e7517f7a774b
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780386"
---
# <a name="restrict-access-to-workers-by-legal-entity"></a>Omezení přístupu k pracovníkům podle právnické osoby

Tento článek vysvětluje, jak nastavit přístup pracovníků podle právnické osoby.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Zaměstnanci jsou zaměstnáni v právnických osobách. Několik příkladů:

- Aaron Con je zaměstnán v právnické osobě USSI.
- Ahmed Barnett je zaměstnán v právnické osobě USMF.
- Alicia Thornber je zaměstnána v právnických osobách GLSI a USMF.

V závislosti na roli uživatele ve společnosti mohou vyžadovat přístup k zobrazení všech zaměstnanců ve všech právnických osobách. Alternativně může být nutné omezit uživatele, aby mohl zobrazit pouze zaměstnance v právnické osobě, ke které má přístup. Chcete-li řídit, které zaměstnance může uživatel zobrazit, vyberte parametr **Omezit přístup k informacím o pracovnících** na stránce **Sdílené parametry Human Resources**.

Uživatel má například přístup ke stránce **Pracovník** a má přístup pouze k právnické osobě USMF. V tomto případě může uživatel zobrazit následující informace o zaměstnancích v předchozím seznamu:

- Pokud není zapnutá funkce pro omezení přístupu k informacím o pracovnících, může uživatel zobrazit informace pro Aarona, Ahmeda a Aliciu.
- Pokud je tato funkce zapnutá, uživatel může zobrazit informace pouze pro Aliciu a Ahmeda, protože jsou také zaměstnáni v právnické osobě USMF.

Zobrazené informace se liší v závislosti na aplikaci, kterou používáte.

## <a name="dynamics-365-human-resources-stand-alone"></a>Samostatné Dynamics 365 Human Resources

Pokud je zapnutá funkce pro omezení přístupu k informacím o pracovníkovi, uvidí uživatel s omezeným přístupem v některých seznamech obsahujících jméno pracovníka prázdnou hodnotu.

Například uživatel, který má přístup pouze k právnické osobě USMF, uvidí následující chování:

- V seznamu **Aktivní pozice** sloupec **Pracovník** bude pro Aaronovu pozici prázdný, protože uživatel nemá přístup k zaměstnancům v právnické osobě USSI.
- Pokud uživatel přejde dolů na jméno pracovníka, zobrazí se prázdná stránka **Pracovník**.

## <a name="dynamics-365-human-resources-on-finance-infrastructure"></a>Dynamics 365 Human Resources na infrastruktuře Finance

Pokud je zapnutá funkce pro omezení přístupu k informacím o pracovníkovi, uvidí uživatel s omezeným přístupem v některých seznamech jméno pracovníka.

Například uživatel, který má přístup pouze k právnické osobě USMF, uvidí následující chování:

- V seznamu **Aktivní pozice** bude ve sloupci **Pracovník** Aaronovo jméno. Pokud uživatel najede myší na jméno pracovníka, zobrazí se pouze jméno a titul.
- Pokud uživatel přejde dolů na jméno pracovníka, zobrazí se prázdná stránka **Pracovník**.

> [!TIP]
> Pokud používáte Dynamics 365 Human Resources na infrastruktuře Finance a chcete, aby uživatelé s omezeným přístupem viděli prázdné hodnoty za jména pracovníků, můžete přidat oprávnění zabezpečení **Omezit přístup pracovníků** pro uživatelské role na stránce **Konfigurace zabezpečení**.

Po zapnutí této funkce musíte provést kroky navíc a nastavit příslušná oprávnění pro každého uživatele, jehož zobrazení musí být omezeno.

1. Na stránce **Uživatelé** vyberte uživatele.
2. Vyberte roli pro uživatele. Možnost **Přiřadit organizace** bude k dispozici.
3. Vyberte **Přiřadit organizace**.
4. Na nové stránce vyberte **Udělit přístup konkrétním organizacím individuálně** a poté vyberte organizace, ke kterým by měl mít uživatel přístup.
5. Opakujte kroky 2 až 4 pro všechny ostatní role, které má uživatel, včetně role uživatele systému.

> [!NOTE]
> Právnické osoby, ke kterým má uživatel přístup, se musí shodovat ve všech rolích uživatele.
