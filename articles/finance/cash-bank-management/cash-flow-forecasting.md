---
title: Prognóza cashflow
description: Toto téma obsahuje přehled procesu prognózy cashflow. Také vysvětluje, jak je prognóza cashflow integrována s jinými moduly v systému.
author: saraschi2
manager: AnnBe
ms.date: 08/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 64d33212600a75900febbd6ec308e4bf5d4f16b7
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645762"
---
# <a name="cash-flow-forecasting"></a>Prognóza cashflow

[!include [banner](../includes/banner.md)]

Nástroje prognózy cashflow můžete používat k analýze nadcházejících měnových a cashflow požadavků, abyste mohli dobře odhadovat nastávající potřeby společnosti na hotovost. K získání prognózy cashflow je nutné dokončit následující kroky:

- Identifikovat a uvést všechny účty likvidity. Účty likvidity jsou účty společnosti pro hotovost nebo ekvivalenty hotovosti.
- Nakonfigurovat chování pro prognózy transakcí, které ovlivňují účty likvidity společnosti.

Po dokončení těchto úloh lze vypočítat a analyzovat prognózy cashflow a nadcházející měnové požadavky.

## <a name="cash-flow-forecasting-integration"></a>Integrace s prognózou cashflow

Prognózu cashflow lze integrovat s moduly Hlavní kniha, Závazky, Pohledávky, Rozpočtování a Řízení zásob. Proces prognózy používá informace o transakcích zadaných do systému a procesu výpočtu prognózuje očekávaný vliv každé transakce na hotovost. Následující typy transakcí jsou zvažovány při výpočtu cashflow:

- **Prodejní objednávky** – Prodejní objednávky, které ještě nebyly fakturovány a jejichž výsledkem jsou fyzické nebo finanční prodeje.
- **Nákupní objednávky** – Nákupní objednávky, které ještě nebyly fakturovány a jejichž výsledkem jsou fyzické nebo finanční nákupy.
- **Pohledávky** – Otevřené transakce odběratele (faktury, které ještě nebyly zaplaceny).
- **Závazky** – Otevřené transakce dodavatele (faktury, které ještě nebyly zaplaceny).
- **Transakce hlavní knihy** – Transakce, kde je určeno, že dojde k budoucímu zaúčtování.
- **Položky registru rozpočtu** – Položky registru rozpočtu, které jsou vybrány pro prognózy cashflow.
- **Prognózy poptávky** – Řádky modelu prognózy zásob, které jsou vybrány pro prognózy cashflow.
- **Prognózy dodávek** – Řádky modelu prognózy zásob, které jsou vybrány pro prognózy cashflow.

Ačkoli neexistuje žádná přímá integrace s řízením a účetnictvím projektu, je k dispozici několik způsobů k zahrnutí transakcí projektu do prognózy cashflow. Zaúčtované projektové faktury jsou zahrnuty do prognózy jako součást otevřených transakcí odběratele. Prodejní a nákupní objednávky iniciované projektem jsou zahrnuty do prognózy jako otevřené objednávky po jejich zadání do systému. Můžete také přenést prognózy projektu do rozpočtového modelu hlavní knihy. Tento rozpočtový model hlavní knihy je poté zahrnut do prognózy cashflow jako součást položek registru rozpočtu.

## <a name="configuration"></a>Konfigurace

Ke konfiguraci procesu prognózy cashflow použijte stránku **Nastavení prognózy cashflow**. Na této stránce určete účty likvidity ke sledování a výchozí chování prognózy pro každou oblast.

### <a name="general-ledger"></a>Hlavní kniha

Nejprve musíte určit účty likvidity, které chcete sledovat prostřednictvím prognózy cashflow. Tyto účty likvidity jsou typicky hlavní účty přidružené k bankovním účtům, které budou přijímat hotovost a z nichž bude hotovost hrazena. Na stránce **Nastavení prognózy cashflow** na kartě **Hlavní kniha** vyberte hlavní účty, které budou zahrnuty do prognózy. Pokud byl bankovní účet přidružen k hlavnímu účtu na stránce **Bankovní účet**, zobrazí se v poli **Bankovní účet**.

Pro hlavní účet můžete nastavit závislou prognózu cashflow obsahující transakce přímo související s transakcemi na jiném hlavním účtu. Každý řádek, který přidáte v části **Závislé účty** vytvoří částku prognózy cashflow na závislém hlavním účtu. Tato částka představuje procento částek cashflow na primárním hlavním účtu, který jste vybrali.

Nejprve nastavte pole **Hlavní účet** na primární hlavní účet, kde podle očekávání dojde nejdříve k transakcím. Nastavte pole **Závislý hlavní účet** na účet, který bude ovlivněn počáteční transakcí proti primárnímu hlavnímu účtu. Pro ostatní pole na řádku nastavte odpovídající hodnoty. Můžete nastavit hodnotu v poli **Procento** tak, aby odrážela vliv primárního hlavní účtu na závislý hlavní účet. Pro prognózu prodeje nebo nákupu vyberte hodnotu **Platební podmínky**, která je typická pro většinu odběratelů nebo dodavatelů. Nastavte pole **Typ zaúčtování** na očekávaný typ zaúčtování, který se vztahuje k prognóze cashflow.

### <a name="accounts-payable"></a>Závazky

Můžete vypočítat prognózu nákupů pomocí možností nastavení na kartě **Závazky** stránky **Nastavení prognózy cashflow**. Před konfigurací prognózy cashflow pro závazky je nutné nakonfigurovat platební podmínky, skupiny dodavatelů a účetní profily dodavatele.

V části **Výchozí údaje prognózy nákupu** lze vybrat výchozí chování při nákupu pro prognózu cashflow. Tři pole určují čas vlivu na hotovost: **Doba mezi datem dodání a datem fakturace**, **Platební podmínky** a **Období mezi datem splatnosti faktury a datem platby**. Prognóza použije výchozí nastavení pro pole **Platební podmínky** pouze v případě, že na transakci není zadána hodnota. Použijte platební podmínku k popisu nejtypičtějšího počtu dní pro každou součást procesu.

Pole **Účty likvidity pro platby** určuje účet likvidity, který se nejčastěji používá pro platby. Použijte pole **Procento částky, které má být přiděleno prognóze cashflow** k určení, zda má být použito během prognózy procento částek. Ponechejte toto pole prázdné, mají-li být použity během prognózy úplné částky transakce.

Můžete přepsat výchozí nastavení pro pole **Období mezi datem splatnosti faktury a datem platby** pro konkrétní skupiny dodavatelů. Prognóza použije výchozí hodnotu z části **Výchozí údaje prognózy nákupu**, pokud není určena odlišná hodnota pro skupinu dodavatelů, která souvisí s dodavatelem na transakci. Chcete-li přepsat výchozí hodnotu, vyberte skupinu dodavatelů a nastavte novou hodnotu pro pole **Čas nákupu**.

Můžete přepsat výchozí nastavení pro pole **Účet likvidity** pro konkrétní účetní profily dodavatelů. Prognóza použije výchozí hodnotu z části **Výchozí údaje prognózy nákupu**, pokud není určen odlišný účet likvidity pro účetní profil, který souvisí s dodavatelem na transakci. Chcete-li přepsat výchozí hodnotu, vyberte účetní profil a zadejte účet likvidity, který bude podle očekávání ovlivněn.

### <a name="accounts-receivable"></a>Pohledávky

Můžete vypočítat prognózu prodeje pomocí možností nastavení na kartě **Pohledávky** stránky **Nastavení prognózy cashflow**. Před konfigurací prognózy cashflow pro pohledávky je nutné nakonfigurovat platební podmínky, skupiny odběratelů a účetní profily odběratelů.

V části **Výchozí údaje prognózy prodeje** lze vybrat výchozí chování při prodeji pro prognózu cashflow. Tři pole určují čas vlivu na hotovost: **Doba mezi datem expedice a datem fakturace**, **Platební podmínky** a **Období mezi datem splatnosti faktury a datem platby**. Prognóza použije výchozí nastavení pro pole **Platební podmínky** pouze v případě, že na transakci není zadána hodnota. Použijte platební podmínku k popisu nejtypičtějšího počtu dní pro každou součást procesu. 

Pole **Účty likvidity pro platby** určuje účet likvidity, který se nejčastěji používá pro platby. Použijte pole **Procento částky, které má být přiděleno prognóze cashflow** k určení, zda má být použito během prognózy procento částek. Ponechejte toto pole prázdné, mají-li být použity během prognózy úplné částky transakce.

Můžete přepsat výchozí nastavení pro pole **Období mezi datem splatnosti faktury a datem platby** pro konkrétní skupiny odběratelů. Prognóza použije výchozí hodnotu z části **Výchozí údaje prognózy prodeje**, pokud není určena odlišná hodnota pro skupinu odběratelů, která souvisí s odběratelem na transakci. Chcete-li přepsat výchozí hodnotu, vyberte skupinu odběratelů a nastavte novou hodnotu pro pole **Čas prodeje**.

Můžete přepsat výchozí nastavení pro pole **Účet likvidity** pro konkrétní účetní profily odběratelů. Prognóza použije výchozí hodnotu z části **Výchozí údaje prognózy prodeje**, pokud není určen odlišný účet likvidity pro účetní profil, který souvisí s odběratelem na transakci. Chcete-li přepsat výchozí hodnotu, vyberte účetní profil a nastavte účet likvidity, který bude podle očekávání ovlivněn.

### <a name="budgeting"></a>Rozpočtování

V prognózách cashflow je možné zahrnout rozpočty, které jsou vytvořeny z rozpočtových modelů. Na kartě **Rozpočtování** stránky **Nastavení prognózy cashflow** vyberte rozpočtové modely, které mají být zahrnuty do prognózy. Ve výchozím nastavení jsou nové položky registru rozpočtu zahrnuty do prognóz poté, co byl povolen rozpočtový model pro prognózu cashflow. Zahrnutí do prognózy cashflow lze u jednotlivých položek registru rozpočtu přepsat.

### <a name="inventory-management"></a>Řízení zásob

Prognózy nabídky a poptávky zásob lze zahrnout do prognóz cashflow. Na kartě **Řízení zásob** stránky **Nastavení prognózy cashflow** vyberte model prognózy, který má být zahrnut do prognózy cashflow. Zahrnutí do prognózy cashflow lze u jednotlivých řádků prognózy nabídky a poptávky přepsat.

### <a name="setting-up-dimensions-for-cash-flow-forecasting"></a>Nastavení dimenzí pro prognózu cashflow
Nová karta na stránce **Nastavení prognózy cashflow** umožňuje řídit, jaké finanční dimenze se mají použít pro filtrování v pracovním prostoru **Prognóza cashflow**. Tato karta se zobrazí, pouze pokud je povolena funkce prognózy cashflow. 

Na kartě **Dimenze** vyberte ze seznamu dimenze, které se mají použít pro filtrování, a pomocí kláves se šipkami je přesuňte do pravého sloupce. Pro filtrování dat prognózy cashflow lze vybrat pouze dvě dimenze. 

### <a name="calculation"></a>Výpočet

Než bude možné zobrazit analýzu prognóz cashflow, je nutné spustit proces výpočtu cashflow. Proces výpočtu bude projektovat budoucí dopady hotovosti zadaných transakcí.

Vypočítejte prognózu cashflow pomocí stránky **Vypočítat prognózy cashflow**. Můžete vypočítat buď prognózu úplného cashflow nebo prognózu přírůstkového cashflow. 

- Chcete-li vymazat všechny transakce prognózy cashflow a provést přepočítání, nastavte pole **Metoda výpočtu prognózy cashflow** na **Celkem**. Doporučujeme, abyste tento postup použili v případě, pokud jste neaktualizovali prognózy cashflow delší dobu. 
- Chcete-li aktualizovat existující informace o cashflow pouze pro nové transakce, nastavte pole **Metoda výpočtu prognózy cashflow** na **Nová**. Na stránce se zobrazí datum, kdy byl naposled spuštěn výpočet cashflow.

Pro své prognózy cashflow můžete také použít dávkové zpracování. K zajištění pravidelných aktualizací analýz prognóz nastavte opakované dávkové zpracování pro výpočet prognózy cashflow.

Ve verzi 10.0.13 bylo vydáno vylepšení procesu výpočtu, které používá rámec automatizace procesů k naplánování úlohy výpočtu cash flow. Toto je povoleno pomocí funkce **Automatizace prognózy peněžních toků** v pracovním prostoru **Správa funkcí**. Po aktivaci vyberte odkaz **Automatizace prognózy peněžních toků** pro zobrazení nové stránky automatizace, kde můžete naplánovat proces výpočtu cash flow. Chcete-li vytvořit nový plán prognózy peněžních toků, vyberte **Vytvořit novou automatizaci procesů** a poté vyberte **Automatizace prognózy peněžních toků** v rozbalovací nabídce **Typ plánu**. Musíte nastavit plán pro každou společnost, pro kterou aktualizujete údaje o prognóze peněžních toků.  Na této stránce je také uvedeno, které úlohy automatizace prognózy peněžních toků čekají a kdy byla dokončena poslední úloha.  

> [!NOTE] 
> Pokud jsou již existující dávkové úlohy naplánovány pro prognózy peněžních toků, zobrazí se chybová zpráva a tuto funkci nebudete moci povolit. Aby bylo možné tuto funkci povolit, bude nutné vymazat stávající dávkové úlohy. 

Další informace naleznete v tématu [Automatizace procesu](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

### <a name="reporting"></a>Vykazování

Po výpočtu prognózy cashflow je nutné obnovit informace o přidružené entitě pro sestavy analýz. Na stránce **Úložiště entit** vyberte měření **Agregace LedgerCovLiquidityMeasurement** a klikněte na **Aktualizovat**.

Existují dva pracovní prostory, které obsahují data prognózy cashflow. Jeden pracovní prostor má data pro všechny společnosti a druhý pracovní prostor má data pouze pro aktuální společnost.

Přístup k pracovnímu prostoru pro všechny společnosti je řízen prostřednictvím funkčního oprávnění **Zobrazit pracovní prostor pro cashflow všech společností**. Ve výchozím nastavení je pracovní prostor **Přehled hotovosti - všechny společnosti** k dispozici pro následující role:

- Výkonný ředitel
- Vedoucí finančního oddělení
- Finanční kontrolor

Přístup k pracovnímu prostoru pro aktuální společnost je řízen prostřednictvím funkčního oprávnění pracovního prostoru **Zobrazit pracovní prostor pro cashflow aktuální společnosti** . Ve výchozím nastavení je pracovní prostor **Přehled hotovosti - aktuální společnost** k dispozici pro následující role:

- Účetní
- Účetní manažer
- Účetní supervizor
- Manažer závazků
- Manažer pohledávek

Pracovní prostor **Přehled hotovosti – všechny společnosti** zobrazuje analýzu prognóz cashflow v systémové měně. Systémová měna a typ směnného kurzu systému, které se používají pro analýzu, jsou definovány na stránce **Systémové parametry**. Tento pracovní prostor zobrazuje přehled prognóz cashflow a zůstatky bankovního účtu pro všechny společnosti. Graf přírůstků a úbytků hotovosti poskytuje přehled pohybů budoucí hotovosti a zůstatky v systémové měně, včetně podrobných informací o předpokládaných transakcích. Také můžete zobrazit předpokládané zůstatky měny.

Pracovní prostor **Přehled hotovosti – aktuální společnost** zobrazuje analýzu prognózy cashflow v definované zúčtovací měně společnosti. Zúčtovací měna, která se používá pro analýzu, se definuje na stránce **Hlavní kniha**. Tento pracovní prostor zobrazuje přehled prognóz cashflow a zůstatky bankovního účtu pro aktuální společnost. Graf přírůstků a úbytků hotovosti poskytuje přehled pohybů budoucí hotovosti a zůstatky v zúčtovací měně, včetně podrobných informací o předpokládaných transakcích. Také můžete zobrazit předpokládané zůstatky měny.

Další informace týkající se analýzy prognózy cashflow naleznete v tématu [Obsah přehledu hotovosti Power BI](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-overview-power-bi-content).

Dále můžete zobrazit data prognózy cashflow pro konkrétní účty, objednávky a položky na následujících stránkách:

- **Předvaha**: Zvolte **Prognózy cashflow** pro zobrazení budoucího cashflow pro vybraný hlavní účet.
- **Všechny prodejní objednávky**: Na kartě **Faktura** zvolte **Prognózy cashflow** pro zobrazení předpokládaného dopadu hotovosti vybrané prodejní objednávky.
- **Všechny nákupní objednávky**: Na kartě **Faktura** zvolte **Prognózy cashflow** pro zobrazení předpokládaného dopadu hotovosti vybrané nákupní objednávky.
- **Prognóza nabídek**: Vyberte **Prognózy cashflow** k zobrazení budoucích cashflow, které jsou přidruženy k vybrané prognóze nabídky položky.
- **Prognóza poptávek**: Vyberte **prognózy cashflow** k zobrazení budoucích cashflow, které jsou přidruženy k vybrané prognóze poptávky položky.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]