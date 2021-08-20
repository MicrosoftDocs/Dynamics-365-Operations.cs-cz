---
title: Konfigurovat úkolový lístek pro zařízení
description: Tohle téma popisuje různé možnosti konfigurace zařízení úkolového lístku.
author: johanhoffmann
ms.date: 05/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch, JmgRegistrationTouchUserConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 9da14c22b0ab62a8384fbe76918cc19da0205cdbbf2f4fd2ef8e7aec57b264ee
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781007"
---
# <a name="configure-job-card-for-devices"></a>Konfigurovat úkolový lístek pro zařízení

[!include [banner](../includes/banner.md)]

Zařízení úkolového lístku používají pracovníci dílny k registraci své každodenní práce, například při zahájení práce, hlášení zpětné vazby o úkolech, registraci nepřímých činností a hlášení nepřítomnosti. Tyto registrace jsou základem pro sledování průběhu a nákladů výrobních zakázek a pro výpočet základu pro odměny pracovníků. Tohle téma popisuje různé možnosti konfigurace zařízení úkolového lístku.

## <a name="enable-new-features-in-feature-management"></a>Povolení nových funkcí ve správě funkcí

Než budou k dispozici, musí být ve vašem systému povoleno několik nastavení popsaných v tomto tématu. Použijte stránku [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) pro povolení některých nebo všech následujících funkcí podle potřeby.

### <a name="generate-license-plate"></a>Generovat poznávací značku

Chcete-li tuto funkci zpřístupnit, povolte následující funkce ve [správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (v pořadí):

1. Registrační značka pro vykazování jako dokončené přidána do zařízení úkolového lístku
1. Povolit automatické generování čísla registrační značky při vykazování jako dokončeno v zařízení úkolového lístku

### <a name="print-label"></a>Tisk etikety

Chcete-li tuto funkci zpřístupnit, povolte následující funkce ve [správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (v pořadí):

1. Registrační značka pro vykazování jako dokončené přidána do zařízení úkolového lístku
1. Vytisknout štítek ze zařízení úkolového lístku

### <a name="allow-locking-of-touch-screen"></a>Povolení uzamčení dotykové obrazovky

Chcete-li tuto funkci zpřístupnit, povolte následující funkci ve [správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- Funkce pro uzamčení zařízení úkolového lístku a terminálu úkolových lístků za účelem dezinfekce

## <a name="manage-your-device-configurations"></a>Správa konfigurace zařízení

Pro nastavení konfigurace zařízení přejděte do nabídky **Řízení výroby > Nastavení > Provádění výroby > Konfigurovat úkolový lístek pro zařízení**. Otevře se stránka **Konfigurace úkolového lístku pro zařízení**, která zobrazuje seznam existujících konfigurací. Zde můžete udělat následující: 

- Výběrem libovolné konfigurace zařízení uvedené v levém sloupci ji zobrazte a upravte.
- Volbou **Nové** v podokně akcí přidejte novou konfiguraci zařízení do seznamu. Poté do pole **Konfigurace** zadejte název, dle kterého identifikujete novou konfiguraci. Hodnota, kterou zde zadáte, musí být ve všech konfiguracích zařízení jedinečná a později ji nebudete moci upravit.

V následujících částech najdete podrobnosti o každém nastavení konfigurace zařízení úkolového lístku.

## <a name="general-settings"></a>Obecné nastavení

Záložka s náhledem **Obecné** umožňuje konfigurovat každou z různých možností dostupných pro vybranou konfiguraci zařízení. K dispozici jsou následující nastavení:

- **Hlášení množství při odchodu** – Nastavením na **Ano** vyzvete pracovníky, aby nahlásili zpětnou vazbu o probíhajících úlohách při odchodu. Při nastavení na **Ne** k tomu pracovníci nebudou vyzváni.
- **Zamknout zaměstnance** – Pokud je tato možnost nastavena na **Ne**, bude každý pracovník odhlášen okamžitě po provedení registrace (jako je nová práce) a zařízení se poté vrátí na přihlašovací stránku. Pokud je tato možnost nastavena na **Ano**, každý pracovník zůstane přihlášený k zařízení úkolového lístku. Pracovník se však bude stále moci odhlásit ručně, aby umožnil jinému pracovníkovi přihlásit se, zatímco zařízení úkolového lístku zůstane spuštěno pod stejným uživatelským účtem systému. Další informace o těchto typech účtů naleznete v tématu [Přiřazení uživatelé](#assigned-users).
- **Čtečka čárových kódů** – Nastavením na **Ano** poskytnete na zařízení úkolového lístku možnost, která zaměstnancům umožní zaregistrovat začátek nové práce naskenováním čárového kódu.
- **Použít skutečný čas registrace** – Nastavením na **Ano** nastavíte čas pro každou novou registraci tak, aby odpovídal přesnému času, kdy pracovník podal registraci. Nastavením na **Ne** se místo toho použije čas přihlášení. Tuto možnost budete obvykle chtít nastavit na **Ano**, pokud jste povolili možnosti **Zamknout zaměstnance** a/nebo **Jeden pracovník**, kde pracovníci často zůstávají přihlášeni delší dobu.
- **Jeden pracovník** – Nastavte tuto možnost na **Ano**, pouze pokud jeden pracovník používá každé zařízení úkolového lístku, kde je tato konfigurace aktivní. Pokud je vybrána tato možnost, možnost **Zamknout zaměstnance** je automaticky nastavena na **Ano**. Tato možnost navíc odstraní požadavek (a schopnost) pracovníka přihlásit se pomocí ID znaku (nebo podobného ID). Místo toho se pracovník přihlásí do Supply Chain Management pomocí systémového uživatelského účtu propojeného s účtem *časově registrovaný pracovník* (z tabulky *pracovníci*) a současně se přihlásí k zařízení úkolového lístku jako tento pracovník.  Další informace o těchto typech účtů naleznete v tématu [Přiřazení uživatelé](#assigned-users).
- **Povolit pracovníkům nastavení osobních filtrů** – Nastavením této možnosti na **Ano** povolíte pracovníkům filtrovat práce, které se jim zobrazují v zařízení. Pracovník může upravit hodnoty pro kterékoli ze tří kritérií filtru: **Výrobní jednotka**, **Skupina prostředků** a **Prostředek**. V zařízení se zobrazí pouze práce naplánované na prostředcích, které odpovídají vybraným kritériím filtru. Můžete také přiřadit výchozí hodnoty kterémukoli nebo všem těmto kritériím a ty budou platit, i když tato možnost nebude vybrána.
- **Povolit uzamčení dotykové obrazovky** – Nastavte tuto možnost na **Ano**, aby pracovníci mohli zamknout dotykovou obrazovku zařízení úkolového lístku, aby ji mohli dezinfikovat. Pokud je možnost povoleno, na přihlašovací stránku zařízení je přidáno tlačítko **Zamknout obrazovku kvůli dezinfekci**. Když pracovník vybere toto tlačítko, dotykový displej se dočasně zamkne, aby se zabránilo neúmyslnému zadání, a zobrazí se odpočítávání. Pracovník může nyní bezpečně vyčistit zařízení a obrazovku. Po skončení odpočítávání se dotykový displej automaticky znovu odemkne.
- **Doba trvání uzamčení obrazovky** – Když je povolena možnost **Povolit uzamčení dotykové obrazovky**, použijte tuto možnost pro zadání počtu sekund, po které by měla být dotyková obrazovka uzamčena pro dezinfekci. Doba trvání musí být mezi 5 a 120 sekundami.
- **Výrobní jednotka** – Vyberte výrobní jednotku, která bude použita jako výchozí kritérium filtru pro seznam prací zobrazovaných každému pracovníkovi. Zařízení zpočátku zobrazí pouze práce naplánované na prostředky seskupené pod vybranou výrobní jednotkou. Pokud je povolena možnost **Povolit pracovníkům nastavení osobních filtrů**, pracovníci budou moci tuto hodnotu upravit, jinak bude tento filtr použit vždy, když je tato konfigurace zařízení aktivní.
- **Skupina prostředků** – Vyberte skupinu prostředků, která bude použita jako výchozí kritérium filtru pro seznam prací zobrazovaných každému pracovníkovi. Zařízení zpočátku zobrazí pouze práce naplánované na prostředky seskupené pod vybranou skupinou prostředků. Pokud je povolena možnost **Povolit pracovníkům nastavení osobních filtrů**, pracovníci budou moci tuto hodnotu upravit, jinak bude tento filtr použit vždy, když je tato konfigurace zařízení aktivní.
- **Prostředek** – Vyberte prostředek, který bude použit jako výchozí kritérium filtru pro seznam prací zobrazovaných každému pracovníkovi. Zařízení zpočátku zobrazí pouze práce naplánované na vybraný prostředek. Pokud je povolena možnost **Povolit pracovníkům nastavení osobních filtrů**, pracovníci budou moci tuto hodnotu upravit, jinak bude tento filtr použit vždy, když je tato konfigurace zařízení aktivní.
- **Generovat registrační značku** – Nastavením této možnosti na **Ano** vygenerujete novou registrační značku pokaždé, když pracovník použije zařízení úkolového lístku k vykázání dokončené práce. Registrační značka vozidla je generována z číselné posloupnosti nastavené na stránce **Parametry řízení skladu**. Při nastavení na **Ne** musí pracovníci při vykazování dokončené práce uvést existující registrační značku.
- **Tisk etikety** – Nastavte tuto možnost na **Ano** k vytištění etikety poznávací značky, když pracovník používá zařízení úkolového lístku k nahlášení dokončené práce. Konfigurace etikety je nastavena ve směrování dokumentu, jak je popsáno v [Rozvržení směrování dokumentu pro popisky registrační značky](../warehousing/document-routing-layout-for-license-plates.md).

<a name="assigned-users"></a>

## <a name="assigned-users"></a>Přiřazení uživatelé

Pomocí záložky s náhledem **Přiřazení uživatelé** přidružíte jednoho nebo více uživatelů systému k aktuální konfiguraci zařízení. Každému uživateli systému lze přiřadit pouze jednu konfiguraci zařízení úlohy.

Při nastavování zařízení se pracovník IT obvykle přihlásí do systému Supply Chain Management pomocí systémového uživatelského účtu. Poté se konfigurace pracovního zařízení přidruženého k tomuto systémovému uživateli použije, dokud zůstane tento systémový uživatel přihlášený. Tyto systémové uživatelské účty jsou obvykle omezeny, aby umožňovaly přístup pouze na stránku zařízení úkolového lístku a do žádné jiné části Supply Chain Management.

Poté, co je systémový uživatel přihlášen a načtena konfigurace pracovního zařízení, mohou se pak pracovníci přihlásit k zařízení úkolového lístku pomocí svého účtu *časově registrovaného pracovníka* (například naskenováním čárového kódu na svém znaku), aby mohli zahájit nové práce a provádět další druhy registrace. Různí pracovníci se mohou přihlásit a odhlásit se během dne, zatímco stejná konfigurace zařízení zůstává v platnosti na tomto počítači, protože systémový uživatel zůstává pro daný den přihlášen k Supply Chain Management.

Jak však bylo uvedeno výše, pokud používáte konfiguraci zařízení s možností **Jeden pracovník**, pracovníci se obvykle přihlásí do systému Supply Chain Management pomocí systémového uživatele propojeného s vlastním účtem *časově registrovaného pracovníka*, takže načtou konfiguraci zařízení a současně se přihlásí jako pracovník na pracovním zařízení.

## <a name="additional-resources"></a>Další prostředky

[Vykázání jako dokončené ze zařízení úkolového lístku](report-finished-job-device.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]