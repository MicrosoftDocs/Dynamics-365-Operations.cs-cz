---
title: Nakonfigurujte roli správce nepřítomnosti
description: Toto téma vysvětluje, jak nastavit roli manažera nepřítomnosti pro správu dovolené zaměstnanců.
author: hasrivas
ms.date: 07/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace, LeaveAbsenceManager
audience: Application User
ms.search.scope: Human Resources
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: hasrivas
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e8a8250b36d2774ac308637253b780592df316cd
ms.sourcegitcommit: 86d38cf57abe768e5bccde48b28280bc2224080c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/19/2021
ms.locfileid: "6639599"
---
# <a name="configure-the-absence-manager-role"></a>Nakonfigurujte roli správce nepřítomnosti

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

V některých organizacích nemusí manažeři lidí spravovat dovolenou pro svůj tým. Místo toho může správce nepřítomnosti tento proces zpracovat pro členy týmu napříč více odděleními a týmy. Manažeři nepřítomnosti mají pro správu dovolené následující funkce:

- Zkontrolovat a schválit volno na základě alternativní hierarchie.
- Zobrazit zůstatky členů týmu.
- Zobrazit kalendář nepřítomnosti.

## <a name="turn-on-the-feature"></a>Zapnutí funkce

1. V pracovním prostoru **Správa systému** vyberte **Správa funkcí**.

2. Na kartě **Správa funkcí** povolte funkci **(Náhled) Správce nepřítomnosti pro správu dovolené**.

## <a name="define-a-custom-hierarchy"></a>Definujte vlastní hierarchii

Funkce správce nepřítomnosti používá vlastní hierarchii, kterou je třeba nakonfigurovat.

1. V pracovním prostoru **Správa organizace** vyberte **Typy hierarchie pozic**.

2. Vytvořte typ hierarchie pozic nazvaný **Dovolená**.

3. V pracovním prostoru **Dovolená a nepřítomnost** pod **Odkazy** vyberte **Parametry dovolené a nepřítomnosti**.

4. Na kartě **Všeobecné** v rozevíracím seznamu **Hierarchie absence** vyberte typ hierarchie **Dovolená**, který jste vytvořili dříve. Toto přidružení hierarchie Dovolená musí být vyplněno pro každou právnickou osobu, kde bude použita funkce správce absencí.

Poté, co je definován typ hierarchie, musí být pozici přiřazena zpráva o hierarchii pozic.

1. V pracovním prostoru **Správa organizace** vyberte **Všechny pozice**.

2. Vyberte pozici, do které chcete přidat hierarchii Dovolená.

3. Na kartě **Vztahy** vyberte **Přidat**.

4. V poli **Název hierarchie** vyberte **Dovolená**.

5. V poli **Nadřízená pozice** vyberte pozici. Po výběru pozice se jméno pracovníka automaticky vyplní.

## <a name="assign-the-absence-manager-role-to-a-user"></a>Přiřaďte uživateli roli nepřítomnosti

Role Správce nepřítomnosti musí být zaměstnancům přidělena, aby jim umožnila schvalovat nebo zamítat žádosti o dovolenou.

1. V pracovním prostoru **Správce systému** vyberte **Odkazy**.

2. V sekci **Uživatelé** vyberte odkaz **Uživatelé**.

3. V seznamu uživatelů vyberte uživatele, kterému chcete přiřadit roli správce nepřítomnosti.

4. Na kartě **Role uživatele** vyberte možnost **Přiřadit role**.

5. V seznamu vyberte roli **Manažer nepřítomnosti**. Pak vyberte **OK**.

    > [!IMPORTANT]
    > Ujistěte se, že role Zaměstnanec byla přiřazena také uživateli, kterému přiřazujete roli Správce nepřítomnosti. Jinak pracovník nebude moci tuto funkci používat.

6. Poté, co jste vytvořili hierarchii Dovolené, ji můžete zobrazit pomocí následujících kroků:

    1. V pracovním prostoru **Správa organizace** vyberte **Hierarchie pozic**.
    
    2. V poli **Typ hierarchie** vyberte **Dovolená**.

## <a name="absence-manager-workspace"></a>Pracovní prostor manažera absencí

V pracovním prostoru **Samoobsluha zaměstnanců** karta **Manažer nepřítomnosti** zobrazuje informace o nepřítomnosti zaměstnanců, kteří jsou v hierarchii Dovolená přiřazeni správci nepřítomnosti.

Na kartě **Dovolená a nepřítomnost** jsou pro každého zaměstnance k dispozici následující možnosti:

- **Volno** - Zobrazit zůstatky, schválené volno a žádosti o volno pro vybraného zaměstnance.
- **Zůstatky dovolené** - Zobrazit seznam zůstatků pro různé plány dovolené pro vybraného zaměstnance.

## <a name="approve-time-off-requests"></a>Schvalování žádostí o volno

Manažeři nepřítomnosti mohou schválit nebo zamítnout žádosti o volno pro zaměstnance. Mohou také podle potřeby vytvářet žádosti jménem zaměstnanců.

> [!IMPORTANT]
> Než mohou manažeři nepřítomnosti schválit nebo zamítnout žádosti o volno, musí být nakonfigurován pracovní postup žádosti o dovolenou tak, aby jim bylo možné přiřadit pracovní položky žádosti o dovolenou ke kontrole.
>
> 1. Na stránce **Pracovní postupy lidských zdrojů** vyberte nebo vytvořte pracovní postup žádosti o dovolenou.
> 2. Vyberte možnost **Přidružená hierarchie** a poté v poli **Název hierarchie** vyberte **Dovolená**.
> 3. Aktualizujte pracovní postup v návrháři pracovního postupu. V **Typu přiřazení** vyberte možnost **Hierarchie** a poté na kartě **Výběr hierarchie** vyberte **Konfigurovatelná hierarchie**.
>
> Další informace o vytváření pracovního postupu žádosti o dovolenou najdete v tématu [Vytvoření pracovního postupu žádosti o dovolenou](hr-leave-and-absence-workflow.md).

1. V pracovním prostoru **Samoobsluha pro zaměstnance** vyberte kartu **Správce nepřítomnosti**.

2. Na kartě **Správce nepřítomnosti** vyberte požadovaného zaměstnance.

3. Vyberte **Podrobnosti** a pak **Volno**.

4. Najděte žádost o volno a vyberte možnost **Schválení**. Poté můžete vybrat možnost schválení nebo zrušení žádosti o volno.

Stav **Zrušení** označuje, že požadavek byl zamítnut. Stav **Dokončeno** označuje, že požadavek byl schválen.

## <a name="view-time-off-in-the-calendar"></a>Zobrazit volno v kalendáři

Uživatelé v roli Správce nepřítomnosti mohou ve svém kalendáři zobrazit žádosti o volno. Chcete-li získat přístup ke kalendáři dovolené, postupujte takto.

> [!IMPORTANT]
> Správce systému musí nakonfigurovat možnosti zobrazení pro kalendář správce nepřítomnosti. Na stránce **Parametry dovolené a nepřítomnosti** na kartě **Kalendář** jsou možnosti, jak skrýt nebo zobrazit narozeniny, absence bez podrobností, dovolené a nevyřízené žádosti o dovolenou. K dispozici je také možnost filtrovat možnost zobrazení kalendáře podle typu pracovníka.

1. V pracovním prostoru **Samoobsluha zaměstnanců** vyberte **Správce nepřítomnosti** a pak **Kalendář správce nepřítomnosti**.

2. Do pole **Datum** zadejte požadované datum.

3. Podle potřeby aktualizujte možnosti zobrazení.

Kalendář správce nepřítomnosti zobrazuje všechny záznamy zaměstnanců, kteří se hlásí správci nepřítomnosti v hierarchii Dovolená.

## <a name="see-also"></a>Viz také

- [Přehled pracovního volna a absencí](hr-leave-and-absence-overview.md)
- [Vytvoření workflow žádosti o pracovní volno](hr-leave-and-absence-workflow.md)
- [Zobrazení kalendáře týmu a společnosti](hr-employee-self-service-calendar.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
