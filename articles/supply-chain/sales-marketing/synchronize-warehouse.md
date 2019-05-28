---
title: Synchronizujte sklady z aplikace Finance and Operations do služby Field Service
description: Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci skladů z Microsoft Dynamics 365 for Finance and Operations do Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 7e6d7626c00b9d7d98ce872652653c36ce7bc975
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1535668"
---
# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a>Synchronizace skladů z aplikace Finance and Operations do služby Field Service

[!include[banner](../includes/banner.md)]

Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci skladů z Microsoft Dynamics 365 for Finance and Operations do Microsoft Dynamics 365 for Field Service.

[![Synchronizace obchodních procesů mezi aplikacemi Finance a Operations and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>Šablony a úkoly
Následující šablona a základní úlohy slouží ke spuštění synchronizace skladů z Microsoft Dynamics 365 for Finance and Operations k Microsoft Dynamics 365 for Field Service.

**Šablona v integraci dat**
- Sklady (Fin and Ops do Field Service)

**Úkol v projektu integrace dat**
- Sklad

## <a name="entity-set"></a>Sada entit
| Field Service    | Finance and Operations                 |
|------------------|----------------------------------------|
| msdyn_warehouses | Sklady                             |

## <a name="entity-flow"></a>Tok entity
Sklady vytvořené a spravované v aplikaci Finance and Operations lze synchronizovat se službu Field Service prostřednictvím projektu integrace dat Common Data Service (CDS). Požadované sklady, které chcete synchronizovat do služby Field Service, je možné v projektu řídit pomocí funkce filtrování a pokročilých dotazů. Sklady, které se synchronizují z aplikace Finance and Operations, jsou vytvořeny ve službě **Field Service, kde je pole Je spravováno externě** nastaveno na **Ano** a záznam je určen pouze pro čtení.

## <a name="field-service-crm-solution"></a>Řešení Field Service CRM
K podpoře integrace mezi moduly Field Service a Finance and Operations jsou požadovány další funkce z řešení služby CRM Field Service. V řešení bylo pole **Je externě udržováno** přidáno do entity **Sklad (msdyn_warehouses)**. Toto pole napomáhá identifikovat, zda je sklad řízen z modulu Finance and Operations nebo zda existuje pouze ve službě Field Service. Nastavení tohoto pole zahrnuje:
- **Ano** – Sklad pochází z aplikace Finance and Operations a nebude ho možné upravovat v aplikaci Sales.
- **Ne** – Sklad byl zadán přímo do služby Field Service a je zde udržován.

Pole **Je externě spravován** pomáhá řídit synchronizaci úrovní zásob, úprav, převody a použití u pracovních příkazů. Pouze sklady se stavem **Je externě spravován** je nastaveno na **Ano** lze použít k synchronizaci přímo ke stejnému skladu v jiném systému. 

> [!NOTE]
> Poznámka: Je možné vytvořit více skladů ve službě Field Service (pomocí **Je externě spravován** = Ne) a poté je namapovat do jediného skladu v aplikaci Finance and Operations pomocí funkce filtrování a pokročilých dotazů. Používá se v situacích, kdy si přejete, aby služba Field Service spravovala podrobné informace o zásobách a jen odesílala aktuální informace do aplikace Finance and Operations. V tomto případě neobdrží služba Field Service aktualizace úrovně zásob z aplikace Finance and Operations. Další informace získáte v části [Synchronizace skladových úprav z aplikace Field Service do Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronizace pracovních příkazů z Field Service na prodejní objednávky navázané na projekt ve Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="prerequisites-and-mapping-setup"></a>Nastavení mapování a předpokladů
### <a name="data-integration-project"></a>Projekt integrace dat
Před synchronizací skladů je nutné aktualizovat rozšířený dotaz a filtrování projektu, aby byly zahrnuty pouze sklady, které chcete převést z aplikace Finance and Operations do služby Field Service. Upozorňujeme, že budete potřebovat sklad ve službě Field Service, abyste jej mohli použít na pracovní příkazy, úpravy a převody.  

Ujistěte se, že **klíč integrace** existuje pro **msdyn_warehouses**:
1. Přjděte na integraci dat.
2. Vyberte kartu **Nastavení připojení**.
3. Vyberte sadu připojení použitou při synchronizaci pracovního příkazu.
4. Vyberte kartu **klíč integrace**.
5. Vyhledejte msdyn_warehouses a potvrďte, že je přidán klíč **msdyn_name (name)**. Pokud se nezobrazuje, přidejte ho kliknutím na tlačítko **Přidat klíč** a klikněte na tlačítko **Uložit** v horní části stránky

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

Na následujícím obrázku je příklad mapování šablony v integraci dat.

### <a name="warehouses-fin-and-ops-to-field-service-warehouse"></a>Sklady (Fin and Ops do Field Service): Sklad

[![Mapování šablony v integraci dat](./media/Warehouse1.png)](./media/Warehouse1.png)
