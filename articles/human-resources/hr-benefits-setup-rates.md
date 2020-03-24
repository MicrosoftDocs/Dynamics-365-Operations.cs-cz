---
title: Konfigurace sazeb
description: Sazby v Microsoft Dynamics 365 Human Resources definují, jakým způsobem přispívají zaměstnavatelé a zaměstnanci k zaměstnanecké výhodě.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f846dcd0a15424ac681dd7e6a229d9da445a54e1
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092400"
---
# <a name="configure-rates"></a>Konfigurace sazeb

[!include [banner](includes/preview-feature.md)]

Sazby v Microsoft Dynamics 365 Human Resources definují, jakým způsobem přispívají zaměstnavatelé a zaměstnanci k zaměstnanecké výhodě. Hodnota může být v závislosti na konfiguraci částka nebo pružné kredity.

Pomocí sazeb lze určit, kolik zaměstnanců a zaměstnavatelů platí na jednotlivé zaměstnanecké výhody na základě několika faktorů. Sazby disponibility jsou efektivní podle data, takže je možné uchovat historické záznamy o sazbách. 

## <a name="set-up-rates"></a>Nastavení sazeb

1. V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Sazby**.

2. Zvolte **Nové**.

3. Zadejte hodnoty pro zbývající pole:

   | Pole | Popis |
   | --- | --- |
   | Kurz | Jedinečný název, který identifikuje sazbu zaměstnanecké výhody. |
   | Popis | Stručný popis sazby zaměstnanecké výhody |
   | Účinné: | Datum, kdy je sazba platná. Výchozí hodnotou je aktuální systémové datum. 
   | Vypršení platnosti | Koncové datum sazby Výchozí hodnota je 12/31/2154 (což znamená nikdy). |
   | Použít úrovně | Úroveň, která má být použita pro výpočet sazby zaměstnaneckých výhod. Jediná úroveň pro jednu sazbu zaměstnaneckých výhod nebo dvojnásobná úroveň pro sazbu zaměstnaneckých výhod dvou úrovní. Příkladem dvojité úrovně je úroveň založená na pohlaví a věku. |
   | Frekvence plateb | Četnost plateb, která určuje, jak často je sazba příplatku na zaměstnanecké výhody placena zprostředkovatelem zaměstnaneckých výhod. Je-li například četnost plateb měsíční, představuje zaměstnanecká sazba měsíční částku platby. |
   | Výpočet sazby platební frekvence | Metoda výpočtu četnosti plateb: standardní nebo roční. |
   | Zaokrouhlení sazby platební frekvence | Způsob zaokrouhlení sazby: standardní nebo zkrácené. |
   | Částka zaměstnance nekuřáka | Částka, kterou poskytovatel zaměstnaneckých výhod účtuje za zaměstnance, který nekouří. Jedná se o částku, kterou zaměstnavatel zaplatí poskytovateli zaměstnaneckých výhod a měla by být založena na četnosti plateb pro nastavení sazby. |
   | Částka zaměstnavatele nekuřáka | Částka, kterou poskytovatel zaměstnaneckých výhod účtuje za zaměstnance, který nekouří. Jedná se o částku, kterou zaměstnavatel zaplatí poskytovateli zaměstnaneckých výhod a měla by být založena na četnosti plateb pro nastavení sazby. |
   | Částka zaměstnance kuřáka | Částka, kterou poskytovatel zaměstnaneckých výhod účtuje za zaměstnance, který kouří. Jedná se o částku, kterou zaměstnavatel zaplatí poskytovateli zaměstnaneckých výhod a měla by být založena na četnosti plateb pro nastavení sazby. |
   | Částka zaměstnavatele kuřáka | Částka, kterou poskytovatel zaměstnaneckých výhod účtuje za zaměstnance, který kouří. Jedná se o částku, kterou zaměstnavatel zaplatí poskytovateli zaměstnaneckých výhod a měla by být založena na četnosti plateb pro nastavení sazby. |
   | Administrativní částka | Správní částka, kterou účtuje správce třetí strany. Jedná se o částku, kterou zaměstnavatel zaplatí správci třetí strany a která by měla by být založena na četnosti plateb pro nastavení sazby. |
   | Sazba flexibilního kreditu | Počet pružných kreditů pro náklady na zaměstnanecké výhody. Tento postup lze použít pouze u plánů zaměstnaneckých výhod, které jsou spojeny s programy pro pružné kredity. Pokud používáte sazby na úrovni vrstvy, je pružný úvěr pro sazbu definován v části Akce > Sazby vrstvy. |
   | Datum platnosti změny | Datum, kdy vstoupí změna sazby zaměstnanecké výhody v platnost. Systém automaticky změní sazbu zaměstnanecké výhody a aktualizuje všechny plány zaměstnaneckých výhod přidružené k této sazbě, pokud spustíte zpracování aktualizace změn frekvence. Toto datum byste měli nastavit pouze v případě, že chcete, aby systém automaticky aktualizoval plány zaměstnaneckých výhod na základě této sazby. Tato možnost je obvykle vyhrazena pro automatické zpracování změny kurzu. Datum účinnosti změny se musí nacházet v rozmezí dat platnosti sazby zaměstnaneckých výhod a v dat vypršení platnosti. |
   | Změna sazby dokončena | Po dokončení změn sazby zaměstnaneckých výhod ve zpracování aktualizace změn sazby bude automaticky zaškrtnuto políčko pro dokončenou změnu sazby. |

4. Chcete-li sledovat a spravovat změny v nastavení sazby zaměstnaneckých výhod, vyberte **Akce** a potom vyberte **Spravovat verze**.

5. Zvolte **Uložit**. 

## <a name="set-up-tier-rates"></a>Nastavení úrovní sazeb

V případě, že se sazba liší v závislosti na různých faktorech, můžete v nastavení sazby použít úrovně sazeb. Můžete například nakonfigurovat úrovně sazeb tak, aby uváděly, že pokud je věk až 34,99, částka pro nekuřáka bude 2. Pokud je věk až 39,99, částka pro nekuřáka je 3.

Můžete také používat dvojí úrovně. Pokud pro hodnotu **Použít úrovně** vyberete **Dvojí úroveň** ve formuláři **Nastavení sazby**, můžete definovat sazby na základě dvou dimenzí. Můžete například nakonfigurovat systém dvojité úrovně tak, aby uváděly, že jste muž ve věku až 34,99, částka pro nekuřáka bude 2. Pokud jste muž ve věku do 39,99, je částka pro nekuřáka 3. Pokud jste žena ve věku do 34,99, je částka pro nekuřáka 1.8. Pokud jste žena ve věku do 39,99, je částka pro nekuřáka 2.8.

1. V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Sazby**.

2. Vyberte jednu nebo více sazeb ze seznamu, vyberte **akce** a pak vyberte možnost **Úrovně sazby**.

3. Zvolte **Nové**.

3. Zadejte hodnoty pro zbývající pole:

   | Pole | Popis |
   | --- | --- | 
   | Popis | Hodnota pole Popis bude použita z popisu v záznamu nastavení sazby. To vám pomůže identifikovat nastavení sazby, ke kterému jsou připojeny sazby úrovně. |
   | Kód úrovní | Vyberte kód úrovně. Kódy úrovní se definují ve formuláři Kódy úrovní. Systém automaticky zobrazí popis kódu úrovně v mřížce vlevo. |
   | Typ úrovně | Určuje, jaké pole má být použito jako kritérium výběru pro proces výpočtu sazby úrovně. Například:</br></br><ul><li>Pokud se použije věk, systém použije datum narození zaměstnance v procesu výpočtu sazby zaměstnaneckých výhod.</li><li>Pokud se použije plat, systém použije roční plat zaměstnaneckých výhod v procesu výpočtu sazby zaměstnaneckých výhod.</li><li>Je-li použit typ práce, systém použije aktuální aktivní záznam pozice zaměstnance k určení typu úlohy podle záznamu úlohy, který je spojený s danou pozicí.</li></ul></br></br>Typy vrstev jsou věk, mzda, fyzické, pohlaví, plný časový ekvivalent, typ práce, oblast kompenzace a úroveň. | 
   | Úroveň | Hodnota, která má být použita s typem vrstvy během procesu výpočtu sazby zaměstnaneckých výhod. Například:</br></br><ul><li>Je-li typem úrovně věk, jedná se o hodnotu stáří.</li><li>Je-li typem úrovně plat, jedná se o částku platu.</li><li> Je-li typem úrovně typ úlohy, jedná se o typ úlohy.</li></ul></br></br>Je-li typem úrovně věk nebo mzda, systém používá při výběru sazby vrstvy vzestupný přístup, což znamená, že hodnota v poli úroveň představuje dolní mez úrovně. S typem vrstvy typu práce systém používá při výběru sazby vrstvy přesný přístup k párování. |
   | Typ výpočtu | Určuje způsob použití částky v poli Částka výpočtu a jaký matematický výpočet bude v případě potřeby proveden. Je-li typem výpočtu paušální částka, systém použije pole s částkami tak, jak je. Je-li typ výpočtu podle částky platu nebo disponibility v USD, systém ve svém matematickém výpočtu použije částku výpočtu a směr výpočtu.</br></br>Je-li typ výpočtu podle částky platu v USD, systém použije následující matematickou rovnici:</br></br>Roční mzda za zaměstnanecké výhody děleno částkou výpočtu (zaokrouhleně nahoru nebo dolů) krát částky pro kuřáky nebo nekuřáky pro zaměstnance nebo zaměstnavatele.</br></br>Je-li typ výpočtu podle částky pokrytí v USD, systém použije následující matematickou rovnici:</br></br>Částka pokrytí děleno částkou výpočtu (zaokrouhleně nahoru nebo dolů) krát částky pro kuřáky nebo nekuřáky pro zaměstnance nebo zaměstnavatele.</br></br>V obou výpočtech se použije způsob výpočtu, který určuje, zda se má zaokrouhlit roční mzda nebo částka disponibility dělená částkou výpočtu nahoru nebo dolů. |
   | Výpočet částky | Částka, která má být použita během procesu výpočtu sazby zaměstnaneckých výhod. Tato částka bude dělitelem při matematickém výpočtu sazby úrovně. |
   | Směr výpočtu | Směr (zvýšení nebo snížení), kterým by měla být výsledná částka zaokrouhlena. Systém podporuje tři směry výpočtu: prázdný (přesná metoda), zvýšení a snížení.</br></br><ul><li>Je-li toto pole prázdné, systém použije přesný výpočet částky mzdy nebo pokrytí vydělené částkou výpočtu. Pokud má tato hodnota zlomek, systém ji použije při výpočtu.</li><li>Pokud je nastaveno zvýšení, systém zvýší matematický výpočet částky mzdy nebo pokrytí vydělený částkou výpočtu na další celé číslo, což znamená, že 12,25 se zvýší na 13.</li><li>Pokud je nastaveno snížení, systém sníží matematický výpočet částky mzdy nebo pokrytí vydělený částkou výpočtu na aktuální celé číslo, což znamená, že 12,25 se sníží na 12.</li></ul> |
   | Částka zaměstnance nekuřáka | Částka, kterou poskytovatel zaměstnaneckých výhod účtuje za zaměstnance, který nekouří. Jedná se o částku, kterou zaměstnavatel zaplatí poskytovateli zaměstnaneckých výhod a měla by být založena na četnosti plateb pro nastavení sazby. |
   | Částka zaměstnavatele nekuřáka | Částka, kterou poskytovatel zaměstnaneckých výhod účtuje za zaměstnance, který nekouří. Jedná se o částku, kterou zaměstnavatel zaplatí poskytovateli zaměstnaneckých výhod a měla by být založena na četnosti plateb pro nastavení sazby. |
   | Částka zaměstnance kuřáka | Částka, kterou poskytovatel zaměstnaneckých výhod účtuje za zaměstnance, který nekouří. Jedná se o částku, kterou zaměstnavatel zaplatí poskytovateli zaměstnaneckých výhod a měla by být založena na četnosti plateb pro nastavení sazby. |
   | Částka zaměstnavatele kuřáka | Částka, kterou poskytovatel zaměstnaneckých výhod účtuje za zaměstnance, který nekouří. Jedná se o částku, kterou zaměstnavatel zaplatí poskytovateli zaměstnaneckých výhod a měla by být založena na četnosti plateb pro nastavení sazby. |
   | Administrativní částka | Správní částka, kterou účtuje správce třetí strany. Jedná se o částku, kterou zaměstnavatel zaplatí správci třetí strany a která by měla by být založena na četnosti plateb pro nastavení sazby. |
   | Sazba flexibilního kreditu nekuřáka | Počet flexibilních kreditů pro náklady na zaměstnanecké výhody na základě výpočtu definovaného pro úroveň úrovně pro nekuřáky. Pokud je například typ výpočtu Na částku pokrytí v USD, částka výpočtu 10 000 a pružný kredit pro nekuřáka je 6, platí, že pokud si zaměstnanec nekuřák vybere krytí 10 000, budou náklady 6 pružných kreditů. Pokud si zvolí pokrytí 20 000 USD, budou nkálady 12 flexibilních kreditů atd. |
   | Sazba flexibilního kreditu kuřáka | Počet flexibilních kreditů pro náklady na zaměstnanecké výhody na základě výpočtu definovaného pro úroveň úrovně pro kuřáky. |

5. Zvolte **Uložit**. 