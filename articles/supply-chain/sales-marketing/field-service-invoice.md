---
title: Synchronizace smluvních faktur v Field Service na volné textové faktury v Supply Chain Management
description: Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci smluvních faktur v Dynamics 365 Field Service do volných faktur v Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 04/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 0942ce83060c186212d7f425f8dbd0a4ca2c09e7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252767"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-supply-chain-management"></a>Synchronizace smluvních faktur v Field Service na volné textové faktury v Supply Chain Management

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci smluvních faktur v Dynamics 365 Field Service do volných faktur v Dynamics 365 Supply Chain Management.

## <a name="templates-and-tasks"></a>Šablony a úkoly

Následující šablona a základní úlohy se používají ke spuštění synchronizace faktur dohod pracovních příkazů v modulu Field Service do prodejních objednávek v modulu Supply Chain Management.

**Název šablony v integraci dat**

- Smluvní faktury (Field Service do Supply Chain Management)

**Názvy úkolů v projektu integrace dat**

- Záhlaví faktury
- Řádky faktury

Následující úlohy synchronizace jsou vyžadovány před zobrazením synchronizace faktur dohod:

- Obchodní vztahy (Sales do Supply Chain Management) – Přímo

## <a name="entity-set"></a>Sada entit

| Field Service  | Správa dodavatelsko-odběratelského řetězce                 |
|----------------|----------------------------------------|
| faktury       | Záhlaví volné faktury Dataverse odběratele |
| invoicedetails | Řádky volné faktury Dataverse odběratele   |

## <a name="entity-flow"></a>Tok entity

Faktury vytvořené z dohody v aplikaci Field Service lze synchronizovat s modulem Supply Chain Management prostřednictvím projektu integrace dat Microsoft Dataverse. Aktualizace těchto faktur budou synchronizovány s volnými textovými fakturami v modulu Supply Chain Management, pokud je stav účtování volné textové faktury **Zpracovává se**. Po zaúčtování volných textových faktur v modulu Supply Chain Management a aktualizaci stavu účetnictví na **Dokončeno** již nemůžete synchronizovat aktualizace z Field Service.

## <a name="field-service-crm-solution"></a>Řešení Field Service CRM

Byl přidán sloupec **Má řádky s původem smlouvy** do tabulky **Faktura**. Tento sloupec pomáhá zajistit, že jsou synchronizovány pouze faktury, které jsou vytvořeny ze smlouvy. Hodnota je **true**, pokud faktura obsahuje alespoň jednu řádku faktury, která pochází z dohody.

Byl přidán sloupec **Má řádky s původem smlouvy** do tabulky **Řádek faktury**. Tento sloupec pomáhá zajistit, že jsou synchronizovány pouze řádky faktury, které jsou vytvořeny ze smlouvy. Hodnota je **true**, pokud řádek faktury pochází z dohody.

**Datum faktury** je povinné pole v modulu Supply Chain Management. Proto musí mít sloupec hodnotu v poli Field Service předtím, než dojde k synchronizaci. Aby bylo možné tento požadavek splnit, je přidána následující logika:

- Pokud je sloupec **Datum faktury** v tabulce **Faktura** prázdné (tj. neobsahuje žádnou hodnotu), je nastaveno na současné datum, když je přidán řádek faktury pocházející ze smlouvy.
- Uživatel může sloupec **Datum faktury** změnit. Avšak pokud se uživatel pokusí uložit fakturu, která pochází ze smlouvy, přijímá chybu obchodního procesu v případě, že je sloupec **datum faktury** na faktuře prázdný.

## <a name="prerequisites-and-mapping-setup"></a>Nastavení mapování a předpokladů

### <a name="in-supply-chain-management"></a>V Supply Chain Management

Původ faktury je nutné nastavit pro integraci, aby bylo možné rozlišit volné textové faktury v modulu Supply Chain Management, které jsou vytvořeny z faktury dohod v modulu Field Service. Když má faktura původ **Integrace faktury dohody**, je pole **Externí faktura** zobrazeno v záhlaví **Prodejní faktura**.

Kromě zobrazení v záhlaví faktury lze použít informace **číslo externí faktury**, které slouží k zajištění, že faktury vytvořené z faktur dohod Field Service jsou filtrovány během synchronizace faktury z Supply Chain Management do Field Service.

1. Přejděte do nabídky **Pohledávky** \> **Nastavení** \> **Kódy původu faktury**.
2. Vyberte **nový** pro vytvoření nového původu faktury.
3. V **Původ faktury** zadejte název pro původní fakturu, jako je například **FS**.
4. Do pole **Popis** zadejte popis, například **Faktura dohody v modulu Field Service**.
5. Zaškrtněte políčko **Přiřazení typů původu**.
6. Nastavte hodnotu v poli **Typ původu faktury** na **Integrace faktury dohody**.
7. Zvolte **Uložit**.

### <a name="in-the-data-integration-project"></a>V projektu Integrace dat

Úloha: **Řádky faktury**  

Ujistěte se, že výchozí hodnota pro pole Supply Chain Management **Zobrazená hodnota hlavního účtu** je aktualizována, aby odpovídala požadované hodnotě.

Výchozí hodnota šablony je **401100**.

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

Na následujícím obrázku je příklad mapování šablony v integraci dat.

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-headers"></a>Smluvní faktury (Field Service do Supply Chain Management): záhlaví faktur

[![Mapování šablony v integraci dat](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-lines"></a>Smluvní faktury (Field Service do Supply Chain Management): řádky faktur

[![Mapování šablony v integraci dat](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]