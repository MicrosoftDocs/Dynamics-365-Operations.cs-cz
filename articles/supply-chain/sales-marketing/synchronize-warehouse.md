---
title: "Synchronizujte sklady z aplikace Finance and Operations do služby Field Service"
description: "Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci skladů z aplikace Microsoft Dynamics 365 for Finance and Operations do aplikace Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 10/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: eb8ba6051777e27bd44504a8160118e8096b1435
ms.contentlocale: cs-cz
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a>Synchronizujte sklady z aplikace Finance and Operations do služby Field Service

[!include[banner](../includes/banner.md)]

Toto téma popisuje šablony a základní úlohy, které se používají k synchronizaci skladů z aplikace Microsoft Dynamics 365 for Finance and Operations do aplikace Microsoft Dynamics 365 for Field Service.

[![Synchronizace obchodních procesů mezi aplikacemi Finance a Operations and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>Šablony a úkoly
Následující šablona a základní úlohy, které se používají k synchronizaci skladů z aplikace Microsoft Dynamics 365 for Finance and Operations do aplikace Microsoft Dynamics 365 or Field Service.

**Název šablony v integraci dat:**
- Sklady (z aplikace Finance and Operations do služby Field Service)

**Názvy úkolů v projektu integrace dat:**
- Sklad

## <a name="entity-set"></a>Sada entit
| Field Service    | Finance and Operations                 |
|------------------|----------------------------------------|
| msdyn_warehouses | Sklady                             |

## <a name="entity-flow"></a>Tok entity
Sklady vytvořené a spravované v aplikaci Finance and Operations lze synchronizovat se službu Field Service prostřednictvím projektu integrace dat Common Data Service (CDS). Požadované sklady, které jsou synchronizovány do služby Field Service, je možné v projektu řídit pomocí funkce filtrování a pokročilých dotazů. Sklady, které se synchronizují z aplikace Finance and Operations, jsou vytvořeny ve službě Field Service, kde je pole externě nastaveno na Ano a záznam je určen pouze pro čtení.
Řešení služby CRM Field Service K podpoře integrace mezi moduly Field Service a Finance and Operations jsou požadovány další funkce z řešení služby CRM Field Service. Řešení obsahuje následující změny.
Pole **udržovány externě je** bylo přidáno do entity **skladu (msdyn_warehouses)**. Toto pole napomáhá identifikovat, zda je sklad řízen operacemi nebo zda existuje pouze ve službě Field Service.
- Ano – Sklad pochází z aplikace Finance and Operations a nebude ho možné upravovat v aplikaci Sales.
- Ne – Sklad byl zadán přímo do služby Field Service a je zde udržován.

Pole **Externě spravován** pomáhá řídit synchronizaci úrovní zásob, úprav, převody a použití u pracovních příkazů. Pouze sklady se stavem **externě spravován** = Ano lze použít k synchronizaci přímo ke stejnému skladu v jiném systému. 

Poznámka: Je možné vytvořit více skladů ve službě Field Service (pomocí **Je externě spravován** = Ne) a poté je namapovat do jediného skladu v aplikaci Finance and Operations pomocí funkce filtrování a pokročilých dotazů. Používá se v situacích, kdy si přejete, aby služba Field Service spravovala podrobné informace o zásobách a jen odesílala aktuální informace do aplikace Finance and Operations. V tomto případě neobdrží služba Field Service aktualizace úrovně zásob z aplikace Finance and Operations. Zobrazit další informace v Synchronizovat úpravy zásob ze služby Field Service do aplikace Finance and Operations a v Synchronizovat pracovní příkazy ve službě Field Service do prodejních objednávce propojených s projektem v aplikaci Finance and Operations.

## <a name="prerequisites-and-mapping-setup"></a>Nastavení mapování a předpokladů
### <a name="in-the-data-integration-project"></a>V projektu Integrace dat
Před synchronizací skladů je nutné aktualizovat rozšířený dotaz a filtrování projektu, aby byly zahrnuty pouze sklady, které chcete převést z aplikace Finance and Operations do služby Field Service. Upozorňujeme, že budete potřebovat sklad ve službě Field Service, abyste jej mohli použít na pracovní příkazy, úpravy a převody.  

Ujistěte se, že **klíč integrace** existuje pro **msdyn_warehouses**
1. Přejít na integraci dat
2. Vyberte kartu **nastavit připojení**.
3. Vyberte sadu připojení použitou při synchronizaci pracovního příkazu
4. Vyberte kartu **klíč integrace**
5. Vyhledejte msdyn_warehouses a zkontrolujte, že je přidán klíč **msdyn_name (name)**. Pokud se nezobrazuje, přidejte ho klepnutím na tlačítko **Přidat klíč** a klepněte na tlačítko **Uložit** v horní části stránky

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

Na následujícím obrázku je příklad mapování šablony v integraci dat.

### <a name="warehouses-finance-and-operations-to-field-service-warehouse"></a>Sklady (z aplikace Finance and Operations do služby Field Service): sklad

[![Mapování šablony v integraci dat](./media/Warehouse1.png)](./media/Warehouse1.png)

