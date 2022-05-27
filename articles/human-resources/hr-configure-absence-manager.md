---
title: Nakonfigurujte roli správce nepřítomnosti
description: Toto téma vysvětluje, jak nastavit roli manažera nepřítomnosti pro správu dovolené zaměstnanců.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace, LeaveAbsenceManager
audience: Application User
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9e7865a0bb33944c803c628f94371a4c75cc38bd
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693024"
---
# <a name="configure-the-absence-manager-role"></a>Nakonfigurujte roli správce nepřítomnosti

>[!Important]
>Funkce uvedené v tomto tématu jsou aktuálně dostupné pro zákazníky používající samostatnou verzi aplikace Dynamics 365 Human Resources. Některé nebo všechny funkce budou dostupné jako součást budoucího vydání na infrastruktury Finance po vydání Finance 10.0.26.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

V některých organizacích nemusí manažeři lidí spravovat dovolenou pro svůj tým. Místo toho může správce nepřítomnosti tento proces zpracovat pro členy týmu napříč více odděleními a týmy. Manažeři nepřítomnosti mají pro správu dovolené následující funkce:

- Zkontrolovat a schválit volno na základě alternativní hierarchie.
- Zobrazit zůstatky členů týmu.
- Zobrazit kalendář nepřítomnosti.

## <a name="turn-on-the-feature"></a>Zapnutí funkce

1. V pracovním prostoru **Správa systému** vyberte **Správa funkcí**.

2. Na kartě **Správa funkcí** povolte funkci **Správce nepřítomnosti pro správu dovolené**.

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

V pracovním prostoru **Samoobsluha zaměstnanců** karta **Správa pracovního volna** zobrazuje informace o nepřítomnosti zaměstnanců, kteří jsou v hierarchii Dovolená přiřazeni správci nepřítomnosti. Správce nepřítomnosti má k dispozici několik možností: 
 - Zkontrolovat žádosti o volno.</br>
 - Odeslat žádost o volno jménem zaměstnance.</br>
 - Zobrazit všechny zaměstnance, kteří jsou mu přiřazeni, jako součást hierarchie volna.</br>
 - Zobrazit kalendář manažera nepřítomnosti.</br>

V pracovním prostoru **Správa pracovného volna** existují dvě karty:
 - **Žádosti o volno**: Na této kartě bude uveden seznam všech nevyřízených žádostí o volno, které může správce nepřítomnosti schválit. Správce nepřítomnosti může vybrat více záznamů a současně s nimi provádět akce. Pokud je povoleno zobrazení volna napříč společnostmi, tento seznam zobrazí nevyřízené žádosti o volno u všech právnických osob, ke kterým mají přístup. V opačném případě zobrazí nevyřízené žádosti o volno aktuálně vybrané právnické osoby. </br>
 - **Všichni zaměstnanci** : Tato karta zobrazí seznam všech zaměstnanců, kteří jsou v hierarchii volna přiřazeni správci nepřítomnosti. Pro každého zaměstnance je k dispozici několik možností:
    - **Požádat o volno** - Odešlete vybranému zaměstnanci novou žádost o volno.</br>
    - **Volno** - Zobrazit zůstatky, schválené volno a žádosti o volno pro vybraného zaměstnance.</br>

## <a name="approve-time-off-requests"></a>Schvalování žádostí o volno

Manažeři nepřítomnosti mohou schválit nebo zamítnout žádosti o volno pro zaměstnance. 

> [!IMPORTANT]
> Než mohou manažeři nepřítomnosti schválit nebo zamítnout žádosti o volno, musí být nakonfigurován pracovní postup žádosti o dovolenou tak, aby jim bylo možné přiřadit pracovní položky žádosti o dovolenou ke kontrole.
>
> 1. Na stránce **Pracovní postupy lidských zdrojů** vyberte nebo vytvořte pracovní postup žádosti o dovolenou.
> 2. Vyberte možnost **Přidružená hierarchie** a poté v poli **Název hierarchie** vyberte **Dovolená**.
> 3. Aktualizujte pracovní postup v návrháři pracovního postupu. V **Typu přiřazení** vyberte možnost **Hierarchie** a poté na kartě **Výběr hierarchie** vyberte **Konfigurovatelná hierarchie**.
>
> Další informace o vytváření pracovního postupu žádosti o dovolenou najdete v tématu [Vytvoření pracovního postupu žádosti o dovolenou](hr-leave-and-absence-workflow.md).

1. V pracovním prostoru **Samoobsluha pro zaměstnance** vyberte kartu **Správa pracovního volna**.

2. Na kartě **Žádosti o volno** vyberte žádosti o volno, se kterými chcete provést akci. V tomto seznamu můžete vybrat více záznamů.

3. Pomocí akčních tlačítek v horní části mřížky můžete žádost o volno schválit, zamítnout nebo delegovat. 

Alternativně může uživatel také použít dlaždici **Žádosti o volno** vlevo pro přechod na seznam všech pracovních položek žádostí o volno. 

## <a name="view-time-off-in-the-calendar"></a>Zobrazit volno v kalendáři

Uživatelé v roli Správce nepřítomnosti mohou ve svém kalendáři zobrazit žádosti o volno. Chcete-li získat přístup ke kalendáři dovolené, postupujte takto.

> [!IMPORTANT]
> Správce systému musí nakonfigurovat možnosti zobrazení pro kalendář správce nepřítomnosti. Na stránce **Parametry dovolené a nepřítomnosti** na kartě **Kalendář** jsou možnosti, jak skrýt nebo zobrazit narozeniny, absence bez podrobností, dovolené a nevyřízené žádosti o dovolenou. K dispozici je také možnost filtrovat možnost zobrazení kalendáře podle typu pracovníka.

1. V samoobslužném pracovním prostoru **Samoobsluha zaměstnanců** vyberte **Správa pracovního volna** a pak **Kalendář správce nepřítomnosti**.

2. Do pole **Datum** zadejte požadované datum.

3. Podle potřeby aktualizujte možnosti zobrazení.

Kalendář správce nepřítomnosti zobrazuje všechny záznamy zaměstnanců, kteří se hlásí správci nepřítomnosti v hierarchii Dovolená.

## <a name="see-also"></a>Viz také

- [Přehled pracovního volna a absencí](hr-leave-and-absence-overview.md)
- [Vytvoření workflow žádosti o pracovní volno](hr-leave-and-absence-workflow.md)
- [Zobrazení kalendáře týmu a společnosti](hr-employee-self-service-calendar.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
