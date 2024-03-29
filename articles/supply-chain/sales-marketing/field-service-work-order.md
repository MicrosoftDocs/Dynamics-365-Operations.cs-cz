---
title: Synchronizace pracovních příkazů ve službě Field Service do prodejních objednávek v aplikaci Supply Chain Management
description: Tento článek popisuje šablony a základní úlohy, které se používají k synchronizaci pracovních příkazů v modulu Field Service do prodejních objednávek v modulu Supply Chain Management.
author: Henrikan
ms.date: 04/09/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: e64c9a954e8f5c4410f8ba370b40b7c6e76e8ae0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860515"
---
# <a name="synchronize-work-orders-in-field-service-to-sales-orders-in-supply-chain-management"></a>Synchronizace pracovních příkazů ve službě Field Service do prodejních objednávek v aplikaci Supply Chain Management

[!include[banner](../includes/banner.md)]



Tento článek popisuje šablony a základní úlohy, které se používají k synchronizaci pracovních příkazů v Dynamics 365 Field Service do prodejních objednávek v Dynamics 365 Supply Chain Management.

[![Synchronizace obchodních procesů mezi Supply Chain Management a Field Service.](./media/field-service-integration.png)](./media/field-service-integration.png)


## <a name="templates-and-tasks"></a>Šablony a úkoly

Následující šablony a základní úlohy se používají k synchronizaci pracovních příkazů v modulu Field Service do prodejních objednávek v Supply Chain Management.

### <a name="names-of-the-templates-in-data-integration"></a>Názvy šablon v integraci dat

Šablona **Pracovní příkazy na prodejní objednávky (Field Service do Supply Chain Management.)** slouží ke spuštění synchronizace.

### <a name="names-of-the-tasks-in-the-data-integration-project"></a>Názvy úkolů v projektu integrace dat

- WorkOrderHeader
- WorkOrderServiceLineEstimate
- WorkOrderServiceLineUsed
- WorkOrderProductLineEstimate
- WorkOrderProductLineUsed

Následující úlohy synchronizace jsou vyžadovány před synchronizací záhlaví prodejní objednávky a mohou se objevit řádky:

- Produkty Field Service (Supply Chain Management do Field Service)
- Obchodní vztahy (Sales do Supply Chain Management) – Přímo

## <a name="entity-set"></a>Sada entit

| **Field Service** | **Správa dodavatelsko-odběratelského řetězce** |
|-------------------------|-------------------------|
| msdyn_workorders        | Záhlaví prodejní objednávky Dataverse |
| msdyn_workorderservices | Řádky prodejní objednávky Dataverse   |
| msdyn_workorderproducts | Řádky prodejní objednávky Dataverse   |

## <a name="entity-flow"></a>Tok entity

Objednávky práce se vytvářejí v aplikaci Field Service. V případě, že objednávky práce zahrnují pouze externě spravované produkty a hodnota **Stav pracovní objednávky** se liší od hodnoty **Neplánované otevřené** a **Uzavřené – zrušené**, lze objednávky práce synchronizovat s Supply Chain Management přes projekt Integrace dat Microsoft Dataverse. Aktualizace u pracovních příkazů budou synchronizovány jako prodejní objednávky v modulu Supply Chain Management. Mezi tyto aktualizace patří informace o typu původu a stavu.

## <a name="estimated-versus-used"></a>Odhadované versus používané

V modulu Field Service mají produkty a služby u pracovních příkazů hodnoty **Odhadované** a **používané** pro množství a částky. V Supply Chain Management ale prodejní objednávky nemají stejný koncept hodnot **Odhadované** a **Používané**. K podpoře přidělení produktu, které používá očekávané množství v prodejní objednávce v Supply Chain Management, ale aby se zachovalo použité množství, které má být spotřebováno a fakturováno, jsou použity dvě sady úkolů k synchronizace produktů a služeb v pracovním příkazu. Jedna skupina úloh je pro hodnoty **Odhadované** a druhá pro hodnoty **Používané**.

Toto chování umožňuje scénáře, kdy se odhadované hodnoty používají pro přidělení nebo rezervace v Supply Chain Management a použité hodnoty pro spotřebu a fakturaci.

### <a name="estimated"></a>Odhadnuto

Pro synchronizaci řádků produktů se hodnoty **odhadované** budou používat, když je hodnota **Stav řádku** **odhadované**, možnost **přidělené** je nastavena na **Ano** a hodnota **Stav systému** není **uzavřen – zaúčtování**.

Pro synchronizaci řádků služby se hodnoty **Odhadované** používají, když je hodnota **Stav řádku** **Odhadované** a **Stav systému** není **Uzavřeno – zaúčtováno**.

### <a name="used"></a>Použito

Hodnoty **Použité** budou použity pro spotřebu a fakturaci. V těchto případech jsou hodnoty **Používá** synchronizovány.

Následující tabulka poskytuje přehled různých kombinací řádků produktu.

| Stav systému <br>(Field Service) | Stav řádku <br>(Field Service) | Přiděleno <br>(Field Service) |Synchronizovaná hodnota <br>(Supply Chain Management) |
|--------------------|-------------|-----------|---------------------------------|
| Otevřeno - Plánováno   | Odhadnuto   | Ano       | Odhadnuto                       |
| Otevřeno - Plánováno   | Odhadnuto   | Ne        | Použito                            |
| Otevřeno - Plánováno   | Použito        | Ano       | Použito                            |
| Otevřeno - Plánováno   | Použito        | Ne        | Použito                            |
| Otevřeno - Probíhá | Odhadnuto   | Ano       | Odhadnuto                       |
| Otevřeno - Probíhá | Odhadnuto   | Ne        | Použito                            |
| Otevřeno - Probíhá | Použito        | Ano       | Použito                            |
| Otevřeno - Probíhá | Použito        | Ne        | Použito                            |
| Otevřeno - Dokončeno   | Odhadnuto   | Ano       | Odhadnuto                       |
| Otevřeno - Dokončeno   | Odhadnuto   | Ne        | Použito                            |
| Otevřeno - Dokončeno   | Použito        | Ano       | Použito                            |
| Otevřeno - Dokončeno   | Použito        | Ne        | Použito                            |
| Zavřeno - Zaúčtováno    | Odhadnuto   | Ano       | Použito                            |
| Zavřeno - Zaúčtováno    | Odhadnuto   | Ne        | Použito                            |
| Zavřeno - Zaúčtováno    | Použito        | Ano       | Použito                            |
| Zavřeno - Zaúčtováno    | Použito        | Ne        | Použito                            |

Následující tabulka poskytuje přehled různých kombinací řádků servisu.

| Stav systému <br>(Field Service) | Stav řádku <br>(Field Service) | Synchronizovaná hodnota <br>(Supply Chain Management) |
|--------------------|-------------|-----------|
| Otevřeno - Plánováno   | Odhadnuto   | Odhadnuto |
| Otevřeno - Plánováno   | Použito        | Použito      |
| Otevřeno - Probíhá | Odhadnuto   | Odhadnuto |
| Otevřeno - Probíhá | Použito        | Použito      |
| Otevřeno - Dokončeno   | Odhadnuto   | Odhadnuto |
| Otevřeno - Dokončeno   | Použito        | Použito      |
| Zavřeno - Zaúčtováno    | Odhadnuto   | Použito      |
| Zavřeno - Zaúčtováno    | Použito        | Použito      |

Synchronizace hodnot **Odhadované** versus **použité** se spravuje pomocí dvou sad úloh pro produktové a servisní řádky. Předdefinované filtry spouští správný úkol a základní mapování pomáhá zaručit, že jsou synchronizovány správné hodnoty **očekávaný** versus **používá se**.

### <a name="example"></a>Příklad

1. V modulu Field Service je vytvořen a naplánován pracovní příkaz.

    Hodnota **Stav systému** je **otevřené – plánované**.

    - **Produktová řada:** odhadované množství = 5ea, použité množství = 0ea, stav řádku = odhad, přidělené = ne.
    - **Řádek servisu:** odhadované množství = 2h, použít množství = 0h, stav řádku = odhad

    V tomto příkladu je hodnota **použité množství** **0** (nula) a hodnota **odhadované množství** služby **2h** jsou synchronizovány v modulu Supply Chain Management.

2. Produkty jsou přiděleny v modulu Field Service.

    Hodnota **Stav systému** je **otevřené – plánované**.

    - **Produktová řada:** odhadované množství = 5ea, použité množství = 0ea, stav řádku = odhad, přidělené = ano.
    - **Řádek servisu:** odhadované množství = 2h, použít množství = 0h, stav řádku = odhad

    V tomto příkladu je hodnota **Odhadované množství** **5ea** a hodnota **Odhadované množství** služby **2h** jsou synchronizovány v modulu Supply Chain Management.

3. Servisní technik začíná pracovat na pracovním příkazu a registruje spotřebu materiálu 6.

    Hodnota **Stav systému** je **otevřené – probíhá**.

    - **Produktová řada:** odhadované množství = 5ea, použité množství = 6ea, stav řádku = použito, přidělené = ano.
    - **Řádek servisu:** odhadované množství = 2h, použít množství = 0h, stav řádku = odhad

    V tomto příkladu je hodnota **Použité množství** **6** a hodnota **odhadované množství** služby **2h** jsou synchronizovány v modulu Supply Chain Management.

4. Servisní technik dokončí pracovní příkaz a registruje dobu používání 1,5 hodin.

    Hodnota **Stav systému** je **otevřené – dokončené**.

    - **Produktová řada:** odhadované množství = 5ea, použité množství = 6ea, stav řádku = použito, přidělené = ano.
    - **Řádek servisu:** odhadované množství = 2 h, použité množství = 1,5 h, stav řádku = použito

    V tomto příkladu je hodnota **použité množství** **6** a hodnota **Použité množství** služby **1,5h** jsou synchronizovány v modulu Supply Chain Management.

## <a name="sales-order-origin-and-status"></a>Původ prodejní objednávky a stavu

### <a name="sales-origin"></a>Původ prodeje

Ke sledování prodejních objednávek, které pocházejí z pracovních příkazů, můžete vytvořit původ prodeje kde je možnost **přiřazení typu původu** nastavena na **Ano** a pole **typ původu prodeje** na **integrace pracovního příkazu**.

Ve výchozím nastavení mapování vybírá původ prodeje pro typ původu prodeje možnost **integrace příkazu práce** pro všechny prodejní objednávky, které jsou vytvořeny z pracovních příkazů. Toto chování může být užitečné při práci s prodejní objednávkou v Supply Chain Management. Ujistěte se, že prodejních objednávky, které pocházejí z pracovních příkazů, nejsou synchronizovány zpět do modulu Field Service jako pracovní příkazy.

Podrobnosti o postupu vytváření správného nastavení původu prodeje v Supply Chain Management získáte v části Předpoklady a nastavení mapování tohoto článku.

### <a name="status"></a>Stav

Když prodejní objednávka vychází z pracovního příkazu, na kartě **Nastavení** záhlaví prodejní objednávky se zobrazí pole **Stav externího pracovního příkazu**. Toto pole zobrazuje stav systému z pracovního příkazu v modulu Field Service na pomoc se sledováním stavu synchronizovaného pracovního příkazu v Supply Chain Management. Toto pole také pomáhá uživateli určit, kdy by měla být prodejní objednávka expedována nebo fakturována.

Pole **Stav externího pracovního příkazu** může obsahovat následující hodnoty:

- Otevřeno - Plánováno
- Otevřeno - Probíhá
- Otevřeno - Dokončeno
- Zavřeno - Zaúčtováno

## <a name="field-service-crm-solution"></a>Řešení Field Service CRM

K podpoře integrace mezi Field Service a Supply Chain Management jsou požadovány další funkce z řešení služby CRM Field Service. Řešení obsahuje následující změny.

### <a name="work-order-entity"></a>Entita pracovního příkazu

Pole **Má pouze externě spravované produkty** bylo přidáno do entity **Pracovní příkaz** a zobrazí se na stránce. Umožňuje konzistentně sledovat, zda pracovní příkaz sestává výhradně z externě spravovaných produktů. Pracovní příkaz sestává zcela z z externě spravovaných produktů, když jsou všechny související produkty uchovávány v Supply Chain Management. Toto pole pomáhá zaručit, že se uživatelé nebudou synchronizovat pracovní příkazy s produkty, které jsou neznámé.

### <a name="work-order-product-entity"></a>Entita produktu pracovního příkazu

- Pole **Objednávka má pouze externě spravované produkty** bylo přidáno do entity **Produkt pracovního příkazu** a zobrazí se na stránce. Umožňuje jednotně sledovat, zda se produkt pracovního příkazu udržuje v Supply Chain Management. Toto pole pomáhá zaručit, že se uživatelé nebudou synchronizovat produkty pracovního příkazu s produkty, které mají v Supply Chain Management neznámé produkty.
- Pole **Stav systému záhlaví** bylo přidáno do entity **Produkt pracovního příkazu** a zobrazí se na stránce. Slouží ke konzistentnímu sledování stavu systému pracovního příkazu a pomáhá zaručit správné filtrování, když jsou produkty pracovního příkazu synchronizovány v Supply Chain Management. Jsou-li filtry nastaveny v integračních úkolech, informace o **stavu systému záhlaví** se také používají k určení, zda mají být synchronizovány odhadované nebo používané hodnoty.
- V poli **Fakturované částky na jednotku** se zobrazí částka, která je fakturována na aktuální jednotce, která se používá. Tato hodnota se vypočítá jako **celková částka** děleno hodnotou **skutečné množství**. Pole se používá pro integraci do systémů, které nepodporují jiné hodnoty pro použité množství a fakturované množství. Toto pole se nezobrazuje v uživatelském rozhraní (UI). 
- Pole **Fakturovaná částka slevy** se počítá jako hodnota **částka slevy** hodnota plus zaokrouhlení z výpočtu **Fakturované částky na jednotku**. Toto pole slouží k integraci a nezobrazuje se v uživatelském rozhraní.
- Pole **Desetinné množství** obsahuje hodnotu z pole **množství** jako desetinné číslo. Toto pole slouží k integraci a nezobrazuje se v uživatelském rozhraní. 
- Hodnota polí **Použito** se resetuje na **0** (nula), když je hodnota **Stav řádku** produktu pracovního příkazu změněna z **Použito** na **Odhadované**. Tato změna umožňuje předcházejí situacím, kdy je omylem zadané množství použité k synchronizaci při nastavení hodnoty **stav řádku** na **odhad** a možnosti **přidělené** na **Ne**.

### <a name="work-order-service-entity"></a>Entita služby pracovního příkazu

- Pole **Objednávka má pouze externě spravované produkty** bylo přidáno do entity **Služba pracovního příkazu** a zobrazí se na stránce. Umožňuje jednotně sledovat, zda se služba pracovního příkazu udržuje v Supply Chain Management. Toto pole pomáhá zaručit, že se uživatelé nebudou synchronizovat služby pracovního příkazu s produkty, které mají v Supply Chain Management neznámé produkty.
- Pole **Stav systému záhlaví** bylo přidáno do entity **Služba pracovního příkazu** a zobrazí se na stránce. Slouží ke konzistentnímu sledování stavu systému pracovního příkazu a pomáhá zaručit správné filtrování, když jsou služby pracovního příkazu synchronizovány v Supply Chain Management. Jsou-li filtry nastaveny v integračních úkolech, informace o **stavu systému záhlaví** se také používají k určení, zda mají být synchronizovány odhadované nebo používané hodnoty.
- Pole **Doba v hodinách** obsahuje hodnotu z pole **trvání** po převodu hodnoty z minut na hodiny. Toto pole slouží k integraci a nezobrazuje se v uživatelském rozhraní.
- Pole **Odhadovaná doba v hodinách** obsahuje hodnotu z pole **odhadované trvání** po převodu hodnoty z minut na hodiny. Toto pole slouží k integraci a nezobrazuje se v uživatelském rozhraní.
- V poli **Fakturované částky na jednotku** se ukládá částka, která je fakturována na aktuální jednotce, která se používá. Tato hodnota se vypočítá jako **celková částka** děleno hodnotou **skutečné množství**. Toto pole se používá pro integraci do systémů, které nepodporují jiné hodnoty pro použité množství a fakturované množství. Toto pole se nezobrazuje v uživatelském rozhraní (UI).
- Pole **Fakturovaná částka slevy** se počítá jako hodnota **částka slevy** hodnota plus zaokrouhlení z výpočtu **Fakturované částky na jednotku**. Toto pole slouží k integraci a nezobrazuje se v uživatelském rozhraní.
- Pole **Externí řádka prodejní objednávky** je vypočtené záporné číslo řádky objednávky, které lze použít v externích systémech, kde jsou zkombinovány pracovní produkty a řádky služby. Toto pole umožňuje produkty pracovního příkazu, které jsou vloženy do kladných čísel řádků a služeb pracovního příkazu, aby měly záporná čísla řádků. Hodnota tohoto pole se vypočítá jako hodnota **řádku prodejní objednávky** krát -1. Toto pole se nezobrazuje v uživatelském rozhraní (UI).
- Hodnota polí **Použito** se resetuje na **0** (nula), když je hodnota **Stav řádku** služby pracovního příkazu z nějakého důvodu změněna z **Použito** na **Odhadované**. Tato změna umožňuje předcházejí situacím, kdy je omylem zadané množství použité k synchronizaci při nastavení hodnoty **stav řádku** na **odhad** a možnosti **stav systému záklaví** he **Zavřeno - zaúčtováno**.

## <a name="preconditions-and-mapping-setup"></a>Nastavení mapování a předpokladů

Před synchronizací pracovních příkazů je důležité aktualizovat následující nastavení v systémech:

### <a name="setup-in-field-service"></a>Nastavení v modulu Field Service

- zajistěte, aby číselné řady používané pro pracovní příkazy v aplikaci Field Service nepřekrývaly číselné řady používané pro prodejní objednávky v Supply Chain Management. V ostatních případech mohou být existující prodejní objednávky nesprávně aktualizovány v modulu Field Service nebo Supply Chain Management.
- Pole **Vytvoření faktury pracovního příkazu** musí být nastaveno na **nikdy**, protože fakturace se provádí v Supply Chain Management. Přejděte na **Field Service** \> **Nastavení** \> **Správa** \> **Nastavení Field Service** a ověřte, že je pole **Vytvoření faktury pracovního příkazu** nastaveno na **Nikdy**.

### <a name="setup-in-supply-chain-management"></a>Nastavení v Supply Chain Management

Integrace pracovního příkazu vyžaduje nastavení původu prodeje. Původ prodej slouží k odlišení prodejních objednávek v Supply Chain Management, které byly vytvořeny z pracovních objednávek v modulu Field Service. Když má prodejní objednávka původ typu **Integrace pracovního příkazu**, v záhlaví prodejní objednávky se zobrazí pole **Stav externí pracovní objednávky**. Původ prodeje, pomáhá zajistit, aby během synchronizace prodejní objednávky z Supply Chain Management do Field Service byly odfiltrovány prodejních objednávek, které byly vytvořeny z pracovních příkazů ve Field Service.

1. Přejděte na **Prodej a marketing** \> **Nastavení** \> **Prodejní objednávky** \> **Původ prodeje**.
2. Vyberte **nový** pro vytvoření nového původu prodeje.
3. V **Původ prodeje** zadejte název pro původ prodeje, jako je například **WorkOrder**.
4. Do pole **Popis** zadejte popis, například **pracovní příkaz v modulu Field Service**.
5. Zaškrtněte políčko **Přiřazení typů původu**.
6. Nastavte hodnotu v poli **Typ původu prodeje** na **Integrace výrobního příkazu**.
7. Zvolte **Uložit**.


### <a name="setup-in-data-integration"></a>Nastavení v integraci dat

Ujistěte se, že **klíč integrace** existuje pro **msdyn_workorders**
1. Přejít na integraci dat
2. Vyberte kartu **nastavit připojení**.
3. Vyberte sadu připojení použitou při synchronizaci pracovního příkazu
4. Vyberte kartu **klíč integrace**
5. Vyhledejte msdyn_workorders a zkontrolujte, že je přidán klíč **msdyn_name (číslo výrobní zakázky)**. Pokud se nezobrazuje, přidejte ho klepnutím na tlačítko **Přidat klíč** a klepněte na tlačítko **Uložit** v horní části stránky

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

Na následujícím obrázku je příklad mapování šablony v integraci dat.

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderheader"></a>Pracovní příkazy so prodejních objednávek (Field Service do Supply Chain Management): WorkOrderHeader

Filtr: (msdyn_systemstatus ne 690970005) a (msdyn_systemstatus ne 690970000) a (msdynce_hasexternallymaintainedproductsonly eq true)

[![Mapování šablon v datové integraci pro pracovní objednávky na prodejní objednávky (Field Service na Supply Chain Management): WorkOrderHeader.](./media/FSWorkOrder1.png )](./media/FSWorkOrder1.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderservicelineestimate"></a>Pracovní příkazy so prodejních objednávek (Field Service do Supply Chain Management): WorkOrderServiceLineEstimate

Filtr: (msdynce_headersystemstatus ne 690970005) a (msdynce_headersystemstatus ne 690970000) a (msdynce_orderhasexternalmaintainedproductsonly eq true) a (msdyn_linestatus eq 690970000) a (msdynce_headersystemstatus ne 690970004)

[![Mapování šablon v datové integraci pro pracovní objednávky na prodejní objednávky (Field Service na Supply Chain Management): WorkOrderServiceLineEstimate.](./media/FSWorkOrder2.png )](./media/FSWorkOrder2.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderservicelineused"></a>Pracovní příkazy so prodejních objednávek (Field Service do Supply Chain Management): WorkOrderServiceLineUsed

Filtr: (msdynce_headersystemstatus ne 690970005) a (msdynce_headersystemstatus ne 690970000) a (msdynce_orderhasexternalmaintainedproductsonly eq true) a ((msdyn_linestatus eq 690970001) nebo (msdynce_headersystemstatus eq 690970004))

[![Mapování šablon v datové integraci pro pracovní objednávky na prodejní objednávky (Field Service na Supply Chain Management): WorkOrderServiceLineUsed.](./media/FSWorkOrder3.png )](./media/FSWorkOrder3.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderproductlineestimate"></a>Pracovní příkazy so prodejních objednávek (Field Service do Supply Chain Management): WorkOrderProductLineEstimate

Filtr: (msdynce_headersystemstatus ne 690970005) a (msdynce_headersystemstatus ne 690970000) a (msdynce_orderhasexternalmaintainedproductsonly eq true) a (msdyn_linestatus eq 690970000) a (msdynce_headersystemstatus ne 690970004) a (msdyn_allocated eq true)

[![Mapování šablon v datové integraci pro pracovní objednávky na prodejní objednávky (Field Service na Supply Chain Management): WorkOrderProductLineEstimate.](./media/FSWorkOrder4.png )](./media/FSWorkOrder4.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderproductlineused"></a>Pracovní příkazy so prodejních objednávek (Field Service do Supply Chain Management): WorkOrderProductLineUsed

Filtr: (msdynce_headersystemstatus ne 690970005) a (msdynce_headersystemstatus ne 690970000) a (msdynce_orderhasexternalmaintainedproductsonly eq true) a ((msdyn_linestatus eq 690970001) nebo (msdynce_headersystemstatus eq 690970004) nebo (msdyn_allocated ne true))

[![Mapování šablon v datové integraci pro pracovní objednávky na prodejní objednávky (Field Service na Supply Chain Management): WorkOrderProductLineUsed.](./media/FSWorkOrder5.png )](./media/FSWorkOrder5.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]