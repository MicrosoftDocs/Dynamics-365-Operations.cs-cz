---
title: Synchronizace smluvních faktur ve službě Field Service do volných faktur v aplikaci Finance and Operations
description: Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci smluvních faktur v Microsoft Dynamics 365 for Field Service do volných faktur v Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 55301ba39dd28fbae5b6c21b1da3c3d9cf6afd8a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "333247"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-finance-and-operations"></a>Synchronizace smluvních faktur ve službě Field Service do volných faktur v aplikaci Finance and Operations

[!include[banner](../includes/banner.md)]

Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci smluvních faktur v Microsoft Dynamics 365 for Field Service do volných faktur v Microsoft Dynamics 365 for Finance and Operations.

## <a name="templates-and-tasks"></a>Šablony a úkoly

Následující šablona a základní úlohy se používají ke spuštění synchronizace faktur dohod pracovních příkazů v modulu Field Service do prodejních objednávek v modulu Finance and Operations.

**Název šablony v integraci dat:**

- Faktury dohod (Field Service do Fin and Ops)

**Názvy úkolů v projektu integrace dat:**

- Záhlaví faktury
- Řádky faktury

Následující úlohy synchronizace jsou vyžadovány před zobrazením synchronizace faktur dohod:

- Účty (Sales do Fin and Ops) - přímé

## <a name="entity-set"></a>Sada entit

| Field Service  | Finance and Operations                 |
|----------------|----------------------------------------|
| faktury       | Záhlaví volné faktury CDS odběratele |
| invoicedetails | Řádky volné faktury CDS odběratele   |

## <a name="entity-flow"></a>Tok entity

Faktury vytvořené z dohody v aplikaci Field Service lze synchronizovat s modulem Finance and Operations prostřednictvím projektu integrace dat Common Data Service (CDS). Aktualizace těchto faktur budou synchronizovány s volnými textovými fakturami v modulu Finance and Operations, pokud je stav účtování volné textové faktury **Zpracovává se**. Po zaúčtování volných textových faktur v modulu Finance and Operations a aktualizaci stavu účetnictví na **Dokončeno** již nemůžete synchronizovat aktualizace z Field Service.

## <a name="field-service-crm-solution"></a>Řešení Field Service CRM

Bylo přidáno pole **Má řádky s původem smlouvy** bylo přidáno do entity **Faktura**. Toto pole pomáhá zajistit, že jsou synchronizovány pouze faktury, které jsou vytvořeny z dohody. Hodnota je **true**, pokud faktura obsahuje alespoň jednu řádku faktury, která pochází z dohody.

Pole **Má původ faktury** bylo přidáno do entity **Řádek faktury**. Toto pole pomáhá zajistit, že jsou synchronizovány pouze řádky faktury, které jsou vytvořeny z dohody. Hodnota je **true**, pokud řádek faktury pochází z dohody.

**Datum faktury** je povinné pole v modulu Finance and Operations. Proto musí mít pole hodnotu v poli Field Service předtím, než dojde k synchronizaci. Aby bylo možné tento požadavek splnit, je přidána následující logika:

- Pokud je pole **Datum faktury** v entitě **Faktura** prázdné (tj. neobsahuje žádnou hodnotu), je nastaveno na současné datum, když je přidán řádek faktury pocházející z dohody.
- Uživatel může pole **Datum faktury** změnit. Avšak pokud se uživatel pokusí uložit fakturu, která pochází z dohody, přijímá chybu obchodního procesu v případě, že je pole **datum faktury** na faktuře prázdné.

## <a name="prerequisites-and-mapping-setup"></a>Nastavení mapování a předpokladů

### <a name="in-finance-and-operations"></a>V aplikaci Finance and Operations

Původ faktury je nutné nastavit pro integraci, aby bylo možné rozlišit volné textové faktury v modulu Finance and Operations, které jsou vytvořeny z faktury dohod v modulu Field Service. Když má faktura původ **Integrace faktury dohody**, je pole **Externí faktura** zobrazeno v záhlaví **Prodejní faktura**.

Kromě zobrazení v záhlaví faktury lze použít informace **číslo externí faktury**, které slouží k zajištění, že faktury vytvořené z faktur dohod Field Service jsou filtrovány během synchronizace faktury z Finance and Operations do Field Service.

1. Přejděte do nabídky **Pohledávky** \> **Nastavení** \> **Kódy původu faktury**.
2. Vyberte **nový** pro vytvoření nového původu faktury.
3. V **Původ faktury** zadejte název pro původní fakturu, jako je například **FS**.
4. Do pole **Popis** zadejte popis, například **Faktura dohody v modulu Field Service**.
5. Zaškrtněte políčko **Přiřazení typů původu**.
6. Nastavte hodnotu v poli **Typ původu faktury** na **Integrace faktury dohody**.
7. Zvolte **Uložit**.

### <a name="in-the-data-integration-project"></a>V projektu Integrace dat

Úloha: **Řádky faktury**  

Ujistěte se, že výchozí hodnota pro pole Finance and Operations **Zobrazená hodnota hlavního účtu** je aktualizována, aby odpovídala požadované hodnotě.

Výchozí hodnota šablony je **401100**.

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

Na následujícím obrázku je příklad mapování šablony v integraci dat.

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-headers"></a>Smluvní faktury (Field Service do Fin a Ops): Záhlaví faktury

[![Mapování šablony v integraci dat](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-lines"></a>Smluvní faktury (Field Service do Fin a Ops): Řádky záhlaví faktury

[![Mapování šablony v integraci dat](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)
