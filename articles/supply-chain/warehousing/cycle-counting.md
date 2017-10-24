---
title: "Cyklická inventura"
description: "Tento článek popisuje postup použití cyklické inventury v rámci řešení skladu, které je k dispozici v modulu Řízení skladu. Tento článek se nevztahuje na skladové řešení, které je k dispozici v modulu Řízení zásob."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSCycleCountThreshold, WHSWorkTableListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 50671
ms.assetid: 49f5c431-b043-4170-aa24-b7d5d1ee063e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2437d3efe7841021ff4bd35f307fddddc76eb4c6
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="cycle-counting"></a>Cyklická inventura

[!include[banner](../includes/banner.md)]


Tento článek popisuje postup použití cyklické inventury v rámci řešení skladu, které je k dispozici v modulu Řízení skladu. Tento článek se nevztahuje na skladové řešení, které je k dispozici v modulu Řízení zásob.

Cyklická inventura je skladový proces, který slouží k auditu skladových položek na skladě. Proces cyklické inventury lze popsat ve třech krocích:

1.  **Vytvoření cyklické inventury** ─ cyklické inventury se vytváří automaticky na základě parametrů prahové hodnoty položek nebo můžete použít plán cyklické inventury. Případně práci cyklické inventury můžete vytvořit ručně pomocí parametrů položky nebo skladu na stránce **Práce cyklické inventury podle zboží** nebo **Práci cyklické inventury podle skladového místa**.
2.  **Zpracování cyklické inventury** ─ po vytvoření cyklické inventury provedete cyklickou inventuru prostřednictvím inventury položek v umístění ve skladu a zadáním výsledku v rámci aplikace Microsoft Dynamics 365 for Finance and Operations pomocí mobilního zařízení. Případně můžete provést inventuru položek v umístění ve skladu, aniž by byla vytvořena cyklická inventura. Tento proces se nazývá *místní cyklická inventura*.
3.  **Vyřešení rozdílu v cyklicky vypočtené hodnotě** ─ po cyklické inventuře budou mít všechny položky, které se liší ve vypočítané hodnotě, stav práce **Čeká na kontrolu** na stránce **Veškerá práce**. Tyto rozdíly můžete vyřešit na stránce **Cyklická inventura práce čeká na kontrolu**.

Následující obrázek znázorňuje proces cyklické inventury. ![Procesní tok pro cyklickou inventuru](./media/performcyclecountinginawarehouselocation.jpg)

## <a name="cycle-counting-prerequisites"></a>Požadavky cyklické inventury
Následující tabulka zobrazuje požadavky, které musí být splněny, než začnete používat cyklickou inventuru.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Předpoklad</th>
<th>Popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Položka</td>
<td>Položky musí být povoleny pro procesy správy skladu.</td>
</tr>
<tr class="even">
<td>Sklad</td>
<td>Sklad musí být povolen pro procesy správy skladu. Pokud chcete povolit sklad pro procesy správy skladu, vyberte na stránce <strong>Sklady</strong> sklad a poté označte možnost <strong>Použít procesy řízení skladu</strong>. Pokud chcete umožnit pracovníkům přepravovat palety při cyklické inventuře na pevné záložce <strong>Řízení skladu</strong> označte pole <strong>Umožnit pohyby palet při cyklické inventuře</strong>.</td>
</tr>
<tr class="odd">
<td>Fondy práce</td>
<td>Volitelné: Vytvořte fond práce a oddělte tak skladovou práci podle typu práce (v tomto případě na práci cyklické inventury).</td>
</tr>
<tr class="even">
<td>Místa</td>
<td>Povolte cyklickou inventuru pro skladová místa. Na stránce <strong>Profily umístění</strong> vyberte možnost <strong>Povolit cyklickou inventuru</strong>, chcete-li povolit cyklickou inventuru pro umístění ve skladu.</td>
</tr>
<tr class="odd">
<td>Parametry řízení skladu</td>
<td>Nastavte parametry pro cyklickou inventuru. Na stránce <strong>Parametry řízení skladu</strong> určete výchozí kód typu úpravy, ID pracovní třídy a pracovní prioritu pro cyklickou inventuru.</td>
</tr>
<tr class="even">
<td>Mobilní zařízení</td>
<td><ul>
<li>Vytvořte položku nabídky pro některou z následujících metod na stránce <strong>Položky nabídky mobilního zařízení</strong>:
<ul>
<li>Cyklická inventura řízená uživatelem</li>
<li>Cyklická inventura řízená systémem</li>
<li>Seskupení cyklické inventury</li>
<li>Místní cyklická inventura</li>
</ul>
</li>
<li>Nastavte nabídku pro mobilní zařízení.</li>
<li>Vytvořte účet pracovního uživatele a přiřaďte nabídku mobilního zařízení k ID pracovního uživatele.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Související úkoly nastavení</td>
<td>Nastavte plán cyklické inventury pro umístění ve skladu.</td>
</tr>
</tbody>
</table>

## <a name="automatically-create-cycle-counting-work"></a>Automaticky vytvořit práci cyklické inventury
Existují dva způsoby, jak lze naplánovat opakované vytvoření cyklické inventury: nastavit prahové hodnoty cyklické inventury nebo nastavit plány cyklické inventury.

-   Prahová hodnota cyklické inventury označuje limit množství nebo procenta skladových položek. Při dosažení omezení prahové hodnoty bude automaticky vytvořena práce cyklické inventury.
-   Plán cyklické inventury vytvoří práce cyklické inventury okamžitě nebo pravidelně skrze dávkovou úlohu. Když je vytvořena práce cyklické inventury, řádek inventurní práce obsahuje informace o skladovém místě, které chcete zahrnout. Zásoby na skladě, které jsou přidružené k danému umístění, nejsou blokovány a jsou tedy k dispozici pro rezervaci a odchozí zpracování, i když existuje otevřená inventurní práce.

### <a name="create-cycle-counting-work-based-on-threshold-parameters-for-items"></a>Vytvoření cyklické inventury na základě parametrů prahové hodnoty pro položky

Cyklickou inventuru lze vytvořit, pokud počet položek klesne pod určitou prahovou hodnotu pro dané umístění. Například existuje 60 položek na skladovém místě, které má prahovou hodnotu cyklické inventury 40. Během transakce prodejní objednávky je 25 položek vyskladněno ze skladového místa a umístěno do přechodného skladového místa. Nový počet položek je o 35 menší, než jaká je prahová hodnota množství, a pro skladové místo je tak automaticky vytvořena cyklická inventura.

### <a name="schedule-cycle-counting-work"></a>Plánování cyklické inventury

Plány cyklické inventury lze nastavit pro vytvoření páce cyklické inventury okamžitě nebo pravidelně. Nastavením plánů cyklické inventury můžete řídit fond práce, pro který je práce cyklické inventury vytvořena, maximální počet cyklických inventur, které jsou vytvořeny pro položky v různých místech, a počet dní před opětovnou inventurou skladového místa. Například položka je k dispozici ve třech umístěních ve skladu, a maximální počet cyklických inventur je nastaven na **2**. V takovém případě když spustíte plán cyklické inventury, vytvoří se dvě práce cyklické inventury pro dvě místa, ve kterých je položka přítomna. Například nastavíte počet dní mezi cyklickou inventurou na **5**. V takovém případě je vytvořena cyklická inventura každých 5 dní. Pokud je však práce cyklické inventury zpracovávána třetího dne, další práce cyklické inventury bude vytvořen pět dnů po zpracování poslední cyklické inventury, osmého dne.

## <a name="create-cycle-counting-work-manually"></a>Vytvoření cyklické inventury ručně
Chcete-li vytvořit práci cyklické inventury ručně, můžete použít stránku **Práce cyklické inventury podle zboží** nebo **Práci cyklické inventury podle skladového místa**. Můžete určit maximální počet cyklických inventur, které lze vytvořit současně. Například pokud vedoucí skladu určí hodnotu **5**, cyklická inventura se vytvoří pro pět umístění i v případě, že se položka nachází v 10 místech. Můžete také vybrat ID fondu práce , do kterého můžete přiřadit ID vytvořené cyklické inventury. Po zpracování ID fondu práce v rámci cyklické inventury se ID cyklické inventury přiřazené k tomuto fondu práce zpracují jako skupina.

## <a name="perform-a-cycle-count-by-using-a-mobile-device"></a>Provedení cyklické inventury pomocí mobilního zařízení
Existuje několik způsobů, jak zpracovat cyklickou inventuru pomocí aplikace Finance and Operations v mobilním zařízení:

-   **Řízené uživatelem** ─ pracovník může zadat ID cyklické inventury uvedené ve stavu **Otevřeno**.
-   **Řízené systémem** ─ aplikace Finance and Operations pracovníkovi přiřadí ID cyklické inventury.
-   **Seskupení cyklické inventury** ─ pracovník může seskupit ID cyklické inventury specifické pro určité místo, zónu nebo fond práce.
-   **Místní cyklická inventura**: pracovník může provádět cyklickou inventuru v umístění ve skladu kdykoliv, aniž by vytvořil cyklickou inventuru. Pokud chcete provádět cyklickou inventuru v daném místě, pracovník musí zadat ID tohoto místa.

Následující postup je uveden jako příklad způsobu provedení místní cyklické inventury pomocí mobilního zařízení. Pokyny, které pracovník uvidí v zařízení, se liší v závislosti na nastavení položky nabídky pro místní cyklickou inventuru.

1.  V mobilním zařízení vyberte položku nabídky a zpracujte tak místní cyklickou inventuru.
2.  Zaregistrujte umístění, pro které chcete provést místní cyklickou inventuru.
3.  Zaregistrujte a potvrďte počet položek a počet položek, u kterých proběhne inventura. **Poznámka:** Stav cyklické inventury se změní na **Čeká na kontrolu** nebo **Zavřeno** na stránce **Veškeré práce** v závislosti na parametrech nastavených na stránce **Pracovník**.
4.  Volitelné: Zopakujte krok 3 pro zbývající položky ve skladovém místě a zkontrolujte, zda nejsou k dispozici žádné další položky pro inventuru.

## <a name="resolve-cycle-counting-differences"></a>Řešení rozdílů v cyklické inventuře
K rozdílům v cyklické inventuře dojde, pokud nastavíte možnost **Je supervizorem cyklické inventury** na **Ne** pro ID pracovního uživatele v těchto případech:

-   Hodnota cyklické inventury není v mezích odchylky uvedených v poli **Maximální limit procent** nebo **Maximální limit množství** na stránce **Uživatelé práce**. Například množství na skladě ve skladovém místě je 50 a limit odchylky uživatele práce je 10. Pokud uživatel práce zadá hodnotu, která není mezi 40 a 60, dojde k rozdílu.
-   Hodnota inventury se liší od množství zásob na skladě a není nastavena mezní odchylka.

Můžete upravit rozdíly ve vypočítané hodnotě, a poté potvrdit vypočítanou hodnotu na stránce **Cyklická inventura čeká na kontrolu**. Upravený počet položek lze ověřit na stránce **Množství na skladě podle skladového místa**. Hodnota inventury bude odmítnuta, pokud rozdíl nelze schválit.

# <a name="see-also"></a>Viz také
[Konfigurace mobilních zařízení pro práci ve skladu](configure-mobile-devices-warehouse.md)




