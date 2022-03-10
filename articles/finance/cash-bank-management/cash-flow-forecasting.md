---
title: Prognóza cashflow
description: Toto téma obsahuje přehled procesu prognózy cashflow. Také vysvětluje, jak je prognóza cashflow integrována s jinými moduly v systému.
author: panolte
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 5a46946ff2c3569dab0ce8b53b3cddcf18318cbf
ms.sourcegitcommit: 465c84eb5cdc211692e2ae09b45d1400f9a315ee
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2022
ms.locfileid: "8314701"
---
# <a name="cash-flow-forecasting"></a>Prognóza cashflow

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Nástroje prognózy cashflow můžete používat k analýze nadcházejících měnových a cashflow požadavků, abyste mohli dobře odhadovat nastávající potřeby společnosti na hotovost. K získání prognózy cashflow je nutné dokončit následující kroky:

- Identifikovat a uvést všechny účty likvidity. Účty likvidity jsou účty společnosti pro hotovost nebo ekvivalenty hotovosti.
- Nakonfigurovat chování pro prognózy transakcí, které ovlivňují účty likvidity společnosti.

Po dokončení těchto úloh lze vypočítat a analyzovat prognózy cashflow a nadcházející měnové požadavky.

## <a name="cash-flow-forecasting-integration"></a>Integrace s prognózou cashflow

Prognózu cashflow lze integrovat s moduly Hlavní kniha, Závazky, Pohledávky, Rozpočtování a Řízení zásob. Proces prognózy používá informace o transakcích zadaných do systému a procesu výpočtu prognózuje očekávaný vliv každé transakce na hotovost. Následující typy transakcí jsou zvažovány při výpočtu cashflow:

- **Prodejní objednávky** – Prodejní objednávky, které ještě nebyly fakturovány a jejichž výsledkem jsou fyzické nebo finanční prodeje.
- **Volné faktury** – Volné faktury, které ještě nejsou zaúčtovány a jejichž výsledkem jsou finanční prodeje. 
- **Nákupní objednávky** – Nákupní objednávky, které ještě nebyly fakturovány a jejichž výsledkem jsou fyzické nebo finanční nákupy.
- **Pohledávky** – Otevřené transakce odběratele (faktury, které ještě nebyly zaplaceny).
- **Závazky** – Otevřené transakce dodavatele (faktury, které ještě nebyly zaplaceny).
- **Transakce hlavní knihy** – Transakce, kde je určeno, že dojde k budoucímu zaúčtování.
- **Položky registru rozpočtu** – Položky registru rozpočtu, které jsou vybrány pro prognózy cashflow.
- **Prognózy poptávky** – Řádky modelu prognózy zásob, které jsou vybrány pro prognózy cashflow.
- **Prognózy dodávek** – Řádky modelu prognózy zásob, které jsou vybrány pro prognózy cashflow.
- **Externí zdroj dat** – Externí data, která jsou zadána nebo importována do prognóz peněžních toků pomocí šablon tabulek.
- **Prognózy projektu** - Řízení projektů a prognózy účetnictví využívající model prognózy.
- **Cashflow – platby z prodeje finančnímu úřadu** – Předpokládané částky plateb daňovému úřadu z prodeje a načasování, jejichž výsledkem jsou finanční platby. Povolte funkci Cashflow – platby z prodeje finančnímu úřadu.

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

V prognózách cashflow je možné zahrnout rozpočty, které jsou vytvořeny z rozpočtových modelů. Ve stránce **Nastavení prognózy cashflow** vyberte na kartě **Rozpočtování** rozpočtové modely, které mají být zahrnuty do prognózy. Ve výchozím nastavení jsou nové položky registru rozpočtu zahrnuty do prognóz poté, co byl povolen rozpočtový model pro prognózu cashflow.

Položky registru rozpočtu lze do prognózy cashflow zahrnout individuálně prostřednictvím personalizace. Když přidáte sloupec „Zahrnout do prognóz cashflow“ do stránky **Položka registru rozpočtu**, systém přepíše nastavení na stránce **Nastavení prognózy cashflow** tak, aby zahrnulo do prognózy záznam individuálního registru rozpočtu.


### <a name="inventory-management"></a>Řízení zásob

Prognózy nabídky a poptávky zásob lze zahrnout do prognóz cashflow. Na kartě **Řízení zásob** stránky **Nastavení prognózy cashflow** vyberte model prognózy, který má být zahrnut do prognózy cashflow. Zahrnutí do prognózy cashflow lze u jednotlivých řádků prognózy nabídky a poptávky přepsat.

### <a name="setting-up-dimensions-for-cash-flow-forecasting"></a>Nastavení dimenzí pro prognózu cashflow
Nová karta na stránce  **Nastavení prognózy cashflow** umožňuje řídit, které finanční dimenze se používají pro filtrování v pracovním prostoru  **Prognóza cashflow**. Tato karta se zobrazí, pouze pokud je povolena funkce prognózy cashflow.

Na kartě **Dimenze** vyberte ze seznamu dimenze, které se mají použít pro filtrování, a pomocí kláves se šipkami je přesuňte do pravého sloupce. Pro filtrování dat prognózy cashflow lze vybrat pouze dvě dimenze. 

### <a name="setting-up-external-source"></a>Nastavení externího zdroje
Externí data lze zadávat nebo importovat do prognóz peněžních toků, když byly konfigurovány přehledy Finance Insights. Před zadáním nebo importem externích dat je třeba nastavit externí zdroje. Na kartě **Vnější zdroj** nastavte externí kategorie peněžních toků. Kategorie může být **Odchozí** nebo **Příchozí**. **Likvidita** by měla být vybrána jako typ účtování. V mřížce **Nastavení právnické osoby** vyberte právnické osoby a odpovídající hlavní účty, na které se vztahují kategorie externích peněžních toků.

Další informace naleznete v tématu [Externí data v prognózách cashflow](../../finance/finance-insights/external-data-in-cash-flow.md). 

### <a name="project-management-and-accounting"></a>Řízení projektů a účetnictví

Ve verzi 10.0.17 umožňuje nová funkce integraci s projektovým řízením a účetnictvím a prognózami cashflow. V pracovním prostoru **Správa funkcí** zapněte funkci **Projektová prognóza cashflow** a přidejte tak předpokládané náklady a výnosy do prognózy cashflow. Na kartě **Řízení projektů a účetnictví** ve stránce **Nastavení prognózy cashflow** vyberte typy projektů a typy transakcí, které mají být zahrnuty do prognózy cashflow. Poté vyberte projektový model prognózy. Dílčí model typu omezení funguje nejlépe. Účty likvidity, které byly zadány v nastavení pohledávek, se používají jako výchozí účty likvidity. Při nastavování prognózy cashflow proto nemusíte zadávat výchozí účty likvidity. Lze také použít rozpočtový model, ale na stránce **Nastavení prognózy cashflow** lze vybrat pouze jeden typ pro projektové řízení a účetnictví. Model prognózy poskytuje největší flexibilitu, když je použito Řízení projektů a účetnictví nebo Project Operations.

Po zapnutí funkce projektové prognózy cashflow lze prognózu cashflow zobrazit pro každý projekt na stránce **Všechny projekty**. V podokně akcí na kartě **Plán** ve skupině **Prognóza** vyberte možnost **Prognóza cashflow**. V pracovním prostoru **Přehled hotovosti** (viz část [Vykazování](#reporting) dále v tomto tématu), zobrazuje typ transakce projektové prognózy přírůstky (výnos projektové prognózy) a úbytky (náklady projektové prognózy). Částky lze zahrnout, pouze pokud **Fáze projektu** v pracovních prostorech **Přehled hotovosti** na nastavena na hodnotu **Zpracovává se**.

Projektové transakce jsou stále několika způsoby zahrnuty do prognózy cashflow, bez ohledu na to, zda je zapnutá funkce **Projektová prognóza cashflow**. Zaúčtované projektové faktury jsou zahrnuty do prognózy jako součást otevřených transakcí odběratele. Prodejní a nákupní objednávky iniciované projektem jsou zahrnuty do prognózy jako otevřené objednávky po jejich zadání do systému. Můžete také přenést prognózy projektu do rozpočtového modelu hlavní knihy. Tento rozpočtový model hlavní knihy je poté zahrnut do prognózy cashflow jako součást položek registru rozpočtu. Pokud jste zapnuli funkci **Projektová prognóza cashflow**, nepřenášejte projektové prognózy do rozpočtového modelu hlavní knihy, protože tato akce způsobí, že se prognózy projektu započítají dvakrát.

### <a name="sales-tax-authority-payments"></a>Platby z prodeje finančnímu úřadu 

Funkce Cashflow – platby z prodeje finančnímu úřadu předpovídá dopad plateb daně z obratu na cashflow. K predikci data a výše plateb cashflow používá nezaplacené transakce DPH, období pro vypořádání daně a platební období zdaňovacího období. 

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

Další informace týkající se analýzy prognózy cashflow naleznete v tématu [Obsah přehledu hotovosti Power BI](Cash-Overview-Power-BI-content.md).

Dále můžete zobrazit data prognózy cashflow pro konkrétní účty, objednávky a položky na následujících stránkách:

- **Předvaha**: Zvolte **Prognózy cashflow** pro zobrazení budoucího cashflow pro vybraný hlavní účet.
- **Všechny prodejní objednávky**: Na kartě **Faktura** zvolte **Prognózy cashflow** pro zobrazení předpokládaného dopadu hotovosti vybrané prodejní objednávky.
- **Všechny nákupní objednávky**: Na kartě **Faktura** zvolte **Prognózy cashflow** pro zobrazení předpokládaného dopadu hotovosti vybrané nákupní objednávky.
- **Prognóza nabídek**: Vyberte **Prognózy cashflow** k zobrazení budoucích cashflow, které jsou přidruženy k vybrané prognóze nabídky položky.
- **Prognóza poptávek**: Vyberte **prognózy cashflow** k zobrazení budoucích cashflow, které jsou přidruženy k vybrané prognóze poptávky položky.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
