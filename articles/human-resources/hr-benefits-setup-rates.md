---
title: Konfigurace sazeb
description: Sazby v Microsoft Dynamics 365 Human Resources definují, jakým způsobem přispívají zaměstnavatelé a zaměstnanci k zaměstnanecké výhodě.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2822f6e339323ca6731ef042ffef3c400ae077d4
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068302"
---
# <a name="configure-rates"></a>Konfigurace sazeb


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Sazby definují, jakým způsobem přispívají zaměstnavatelé a zaměstnanci k zaměstnanecké výhodě. Hodnota může být v závislosti na konfiguraci částka nebo několik flexibilních kreditů.

Pomocí sazeb lze určit, kolik zaměstnanců a zaměstnavatelů platí na jednotlivé zaměstnanecké výhody na základě několika faktorů. Sazby disponibility jsou efektivní podle data, takže je možné uchovat historické záznamy o sazbách. 

## <a name="set-up-rates"></a>Nastavení sazeb

1. V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Sazby**.

2. Zvolte **Nové**.

3. Zadejte hodnoty pro zbývající pole:

   | Pole | Popis |
   | --- | --- |
   | **Kurz** | Jedinečný název, který identifikuje sazbu zaměstnanecké výhody. |
   | **Popis** | Stručný popis sazby zaměstnanecké výhody |
   | **Účinné:** | Datum, od kterého je sazba platná. Výchozí hodnotou je aktuální systémové datum. Toto datum by mělo být stejné nebo dříve než vaše období výhod. Dobrým postupem je nastavit toto datum na datum plánu dávek. |
   | **Vypršení platnosti** | Koncové datum sazby Výchozí hodnota je 12/31/2154 (což znamená nikdy). |
   | **Použít úrovně** |  Toto pole použijte, pokud máte logiku, která musí být použita k určení sazby. Pokud se například sazba musí zvýšit na základě věku, vyberte zde hodnotu. Vyberte **Jediná úroveň** pro jednu sazbu zaměstnaneckých výhod nebo **dvojitá úroveň** pro sazbu zaměstnaneckých výhod dvou úrovní. Příkladem dvojité úrovně je úroveň založená na pohlaví a věku. Po výběru hodnoty vyberte **Akce** a potom vyberte **Úrovně sazeb**. Pokud máte paušální sazbu, která se nemění, nechte toto pole prázdné. |
   | **Četnost plateb** | Uveďte, jak často by měla být sazba pojistného na dávky vyplácena poskytovateli dávek. Sazby, které zadáte na stránce popsané dále v tomto tématu, budou založeny na frekvenci plateb, kterou zde zadáte. Například pokud zadáte **Měsíční** do tohoto pole a zadáte sazbu pro zaměstnance ve výši **100 $**, předpokládá se, že výhoda bude zaměstnance stát $100 měsíčně. Zaměstnanec však může být placen dvakrát za měsíc na základě četnosti výplat dávek, která je nastavena v záznamu zaměstnance. V tomto případě, když se zaměstnanec přihlásí k **samoobsluze zaměstnanců**, bude částka, kterou zaplatí, $50, protože sazba, kterou **samoobsluha zaměstnanců** zobrazuje, je založena na frekvenci plateb zaměstnance. |
   | **Zaokrouhlení sazby platební frekvence** | Metody zaokrouhlování kurzu jsou: Standardní, Zkrácené, Normální, Dolů a Zaokrouhlování nahoru. </br></br><ul><li>**Standard** - Vždy zaokrouhlit nahoru. Například 10,611 se zaokrouhlí na 10,62. -10,231 se zaokrouhlí na -10,23. </li><li>**Zkráceno** - Vždy zaokrouhlit dolů. Například 10,619 se zaokrouhlí na 10,61. -10,231 se zaokrouhlí na -10,24. </li><li>**Normální** - Desetinná místa končící nebo větší než 5 se zaokrouhlují směrem od nuly. Desetinné hodnoty končící na nebo menší než 4 se zaokrouhlují na nulu. Například 10,615 se zaokrouhlí na 10,62. -10,235 se zaokrouhlí na -10,24. 10,614 se zaokrouhlí na 10,61. -10,234 se zaokrouhlí na -10,23. </li><li>**Dolů** - Zaokrouhlit na nulu. Například 10,619 se zaokrouhlí na 10,61. -10,231 se zaokrouhlí na -10,23. </li><li>**Zaokrouhlování nahoru** - Zaokrouhlení nahoru. Například 10,619 se zaokrouhlí na 10,62. -10,231 se zaokrouhlí na -10,24. |
   | **Částka zaměstnance nekuřáka** | Částka, kterou poskytovatel zaměstnaneckých výhod účtuje za zaměstnance, který nekouří. Jedná se o částku, kterou zaměstnavatel zaplatí poskytovateli zaměstnaneckých výhod a měla by být založena na četnosti plateb pro nastavení sazby. |
   | **Částka zaměstnavatele nekuřáka** | Částka, kterou poskytovatel zaměstnaneckých výhod účtuje za zaměstnance, který nekouří. Jedná se o částku, kterou zaměstnavatel zaplatí poskytovateli zaměstnaneckých výhod a měla by být založena na četnosti plateb pro nastavení sazby. |
   | **Částka zaměstnance kuřáka** | Částka, kterou poskytovatel zaměstnaneckých výhod účtuje za zaměstnance, který kouří. Jedná se o částku, kterou zaměstnavatel zaplatí poskytovateli zaměstnaneckých výhod a měla by být založena na četnosti plateb pro nastavení sazby. |
   | **Částka zaměstnavatele kuřáka** | Částka, kterou poskytovatel zaměstnaneckých výhod účtuje za zaměstnance, který kouří. Jedná se o částku, kterou zaměstnavatel zaplatí poskytovateli zaměstnaneckých výhod a měla by být založena na četnosti plateb pro nastavení sazby. |
   | **Administrativní částka** | Správní částka, kterou účtuje správce třetí strany. Jedná se o částku, kterou zaměstnavatel zaplatí správci třetí strany a která by měla by být založena na četnosti plateb pro nastavení sazby. |
   | **Sazba flexibilního kreditu** | Počet pružných kreditů pro náklady na zaměstnanecké výhody. Tento postup lze použít pouze u plánů zaměstnaneckých výhod, které jsou spojeny s programy pro pružné kredity. Pokud používáte sazby na úrovni vrstvy, je pružný úvěr pro sazbu definován v části Akce > Sazby vrstvy. |
   | **Datum platnosti změny** | Datum, kdy vstoupí změna sazby zaměstnanecké výhody v platnost. Systém automaticky změní sazbu zaměstnanecké výhody a aktualizuje všechny plány zaměstnaneckých výhod přidružené k této sazbě, pokud spustíte zpracování aktualizace změn frekvence. Toto datum nenastavujte v případě, že chcete, aby systém automaticky aktualizoval plány zaměstnaneckých výhod na základě této sazby. Tato možnost je obvykle vyhrazena pro automatické zpracování změny kurzu. **Datum účinnosti změny** se musí nacházet v rozmezí dat platnosti sazby zaměstnaneckých výhod a v dat vypršení platnosti. |
   | **Změna sazby dokončena** | Po dokončení změn sazby zaměstnaneckých výhod ve zpracování aktualizace změn sazby bude automaticky zaškrtnuto políčko **Změna sazby dokončena**. |

4. Chcete-li sledovat a spravovat změny v nastavení sazby zaměstnaneckých výhod, vyberte **Akce** a potom vyberte **Spravovat verze**.

5. Zvolte **Uložit**. 

## <a name="set-up-tier-rates"></a>Nastavení úrovní sazeb

V případě, že se sazba liší v závislosti na různých faktorech, můžete v nastavení sazby použít úrovně sazeb. Můžete například nakonfigurovat úrovně sazeb tak, aby uváděly, že pokud je věk až 34,99, částka pro nekuřáka bude 2. Pokud je věk až 39,99, částka pro nekuřáka je 3.

Můžete také používat dvojí úrovně. Pokud pro hodnotu **Použít úrovně** vyberete **Dvojí úroveň** ve formuláři **Nastavení sazby**, můžete definovat sazby na základě dvou dimenzí. Můžete například nakonfigurovat systém dvojité úrovně tak, aby uváděly, že jste muž ve věku až 34,99, částka pro nekuřáka bude 2. Pokud jste muž ve věku do 39,99, je částka pro nekuřáka 3. Pokud jste žena ve věku do 34,99, je částka pro nekuřáka 1.8. Pokud jste žena ve věku do 39,99, je částka pro nekuřáka 2.8.

> [!IMPORTANT]
> Možnost v **Osobní informace** v záznamu pracovníka se používá k označení, zda je zaměstnanec kuřák. Pokud je zaměstnanec zaznamenán jako kuřák, použije se kuřácká sazba. (Označení kuřáka se zaměstnanci nikdy nezobrazí.)
   
1. V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Sazby**.

2. Vyberte jednu nebo více sazeb ze seznamu, vyberte **akce** a pak vyberte možnost **Úrovně sazby**.

3. Zvolte **Nové**.

3. Zadejte hodnoty pro zbývající pole:

   | Pole | popis |
   | --- | --- | 
   | **Popis** | Hodnota pole **Popis** je použita z popisu v záznamu nastavení sazby. To vám pomůže identifikovat nastavení sazby, ke kterému jsou připojeny sazby úrovně. |
   | **Kód úrovní** | Vyberte kód úrovně. Kódy úrovní se definují na stránce **Kódy úrovní**. Systém automaticky zobrazí popis kódu úrovně v mřížce vlevo. |
   | **Typ úrovně** | Určuje, jaké pole má být použito jako kritérium výběru pro proces výpočtu sazby úrovně. Například:</br></br><ul><li>Pokud se použije **Věk**, systém použije datum narození zaměstnance v procesu výpočtu sazby zaměstnaneckých výhod.</li><li>Pokud se použije **Plat**, systém použije roční plat zaměstnaneckých výhod v procesu výpočtu sazby zaměstnaneckých výhod.</li><li>Je-li použit **Typ práce**, použije se aktuální aktivní záznam pozice zaměstnance k určení typu úlohy podle záznamu úlohy, který je spojený s danou pozicí.</li></ul></br></br>Typy úrovní jsou **Věk**, **Plat**, **Fyzické**, **Pohlaví**, **Plný časový ekvivalent**, **Typ práce**, **Oblast kompenzace** a **Úroveň**. | 
   | **Úroveň** | Hodnota, která má být použita s typem vrstvy během procesu výpočtu sazby zaměstnaneckých výhod. Například:</br></br><ul><li>Je-li typem úrovně **Věk**, jedná se o hodnotu stáří.</li><li>Je-li typem úrovně **Plat**, jedná se o částku platu.</li><li> Je-li typem úrovně **Typ práce**, jedná se o typ práce.</li></ul></br></br>Je-li typem úrovně **Věk** nebo **Plat**, hodnota v poli **Úroveň** představuje horní hranici úrovně. S typem úrovně **Typ práce** se používá při výběru sazby úrovně přístup přesné shody. |
   | **Typ výpočtu** | Určuje způsob použití částky v poli Částka výpočtu a jaký matematický výpočet bude v případě potřeby proveden. Je-li typem výpočtu paušální částka, systém použije pole s částkami tak, jak je. Je-li typ výpočtu podle částky platu nebo disponibility v USD, systém ve svém matematickém výpočtu použije částku výpočtu a směr výpočtu.</br></br>Je-li typ výpočtu podle částky platu v USD, se použije následující matematická rovnice:</br></br>Roční mzda za zaměstnanecké výhody děleno částkou výpočtu (zaokrouhleně nahoru nebo dolů) krát částky pro kuřáky nebo nekuřáky pro zaměstnance nebo zaměstnavatele.</br></br>Je-li typ výpočtu podle částky pokrytí v USD, se použije následující matematická rovnice:</br></br>Částka pokrytí děleno částkou výpočtu (zaokrouhleně nahoru nebo dolů) krát částky pro kuřáky nebo nekuřáky pro zaměstnance nebo zaměstnavatele.</br></br>V obou výpočtech se použije způsob výpočtu, který určuje, zda se má zaokrouhlit roční mzda nebo částka disponibility dělená částkou výpočtu nahoru nebo dolů. |
   | **Výpočet částky** | Částka, která má být použita během procesu výpočtu sazby zaměstnaneckých výhod. Tato částka bude dělitelem při matematickém výpočtu sazby úrovně. |
   | **Směr výpočtu** | Směr, kterým by měla být výsledná částka zaokrouhlena. Systém podporuje tři směry výpočtu: prázdný (přesná metoda), **zvýšení** a **snížení**.</br></br><ul><li>Je-li toto pole prázdné, systém použije přesný výpočet částky mzdy nebo pokrytí vydělené částkou výpočtu. Pokud má tato hodnota zlomek, použije se při výpočtu.</li><li>Pokud je nastaveno **Zvýšení**, zvýší se matematický výpočet částky mzdy nebo pokrytí vydělený částkou výpočtu na další celé číslo, což znamená, že 12,25 se zvýší na 13.</li><li>Pokud je nastaveno **Snížení**, sníží se matematický výpočet částky mzdy nebo pokrytí vydělený částkou výpočtu na aktuální celé číslo, což znamená, že 12,25 se sníží na 12.</li></ul> |
   | **Částka zaměstnance nekuřáka** | Částka, kterou poskytovatel zaměstnaneckých výhod účtuje za zaměstnance, který nekouří. Jedná se o částku, kterou zaměstnavatel zaplatí poskytovateli zaměstnaneckých výhod a měla by být založena na četnosti plateb pro nastavení sazby. |
   | **Částka zaměstnavatele nekuřáka** | Částka, kterou poskytovatel zaměstnaneckých výhod účtuje za zaměstnance, který nekouří. Jedná se o částku, kterou zaměstnavatel zaplatí poskytovateli zaměstnaneckých výhod a měla by být založena na četnosti plateb pro nastavení sazby. |
   | **Částka zaměstnance kuřáka** | Částka, kterou poskytovatel zaměstnaneckých výhod účtuje za zaměstnance, který nekouří. Jedná se o částku, kterou zaměstnavatel zaplatí poskytovateli zaměstnaneckých výhod a měla by být založena na četnosti plateb pro nastavení sazby. |
   | **Částka zaměstnavatele kuřáka** | Částka, kterou poskytovatel zaměstnaneckých výhod účtuje za zaměstnance, který nekouří. Jedná se o částku, kterou zaměstnavatel zaplatí poskytovateli zaměstnaneckých výhod a měla by být založena na četnosti plateb pro nastavení sazby. |
   | **Administrativní částka** | Správní částka, kterou účtuje správce třetí strany. Jedná se o částku, kterou zaměstnavatel zaplatí správci třetí strany a která by měla by být založena na četnosti plateb pro nastavení sazby. |
   | **Sazba flexibilního kreditu nekuřáka** | Počet flexibilních kreditů pro náklady na zaměstnanecké výhody na základě výpočtu definovaného pro úroveň úrovně pro nekuřáky. Pokud je například typ výpočtu **Na částku pokrytí v USD**, částka výpočtu 10 000 a pružný kredit pro nekuřáka je 6, platí, že pokud si zaměstnanec nekuřák vybere krytí 10 000, budou náklady 6 pružných kreditů. Pokud si zvolí pokrytí 20 000 USD, budou nkálady 12 flexibilních kreditů atd. |
   | **Sazba flexibilního kreditu kuřáka** | Počet flexibilních kreditů pro náklady na zaměstnanecké výhody na základě výpočtu definovaného pro úroveň úrovně pro kuřáky. |

5. Zvolte **Uložit**. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
