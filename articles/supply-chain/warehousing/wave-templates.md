---
title: Šablony vlny
description: Toto téma popisuje, jak nastavit kritéria určující, zda jsou vlny zpracovány ručně nebo automaticky, a práci, která vznikne pro sklad při zpracování vlny.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: aca03e3fda4405fa6fe2b427a47066af5bb95b644b7f5b47d22736347208a8bd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751618"
---
# <a name="wave-templates"></a>Šablony vlny

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak nastavit kritéria určující, zda jsou vlny zpracovány ručně nebo automaticky, a práci, která vznikne pro sklad při zpracování vlny. Podle potřeby určete kritéria nastavením šablon vlny a dotazů, které odpovídají vlně ve vydaných řádcích u prodejní objednávky, výrobní zakázky a kanbanů.

## <a name="settings-for-wave-templates"></a>Nastavení šablon vlny

Při nastavení šablony vlny je třeba zadat následující:

- **Lokalita** a **Sklad**, pro který vytvoří šablona práci.
- Pořadí, v jakém budou šablony vyhodnocovány. Pořadí, ve kterém budou šablony odpovídat vydaným řádkům z prodejních objednávek, výrobních zakázek a kanbanů. Když je řádek uvolněn, systém použije první šablonu vlny, pro kterou řádek splňuje kritéria. Čím širší jsou kritéria, tím je pravděpodobnější, že je řádek splní, proto byste měli na začátek seznamu umístit šablony s co nejkonkrétnějšími kritérii. Použijte tlačítka **Nahoru** a **Dolů** v podokně akcí pro uspořádání šablon v seznamu.
- Akce provedené každou šablonou. **Metody** vlny, které provádějí akce vytvořené šablonou, jako např. vytváření nebo rozdělení práce pro každý typ šablony vlny.
- Atributy vln (filtry), které musí platit pro šablonu vlny, která má být použita.

> [!NOTE]
> V případě potřeby může vývojář vytvořit další metody. Celý seznam metod si můžete prohlédnout na stránce **Metody zpracování vlny**.

Některá následující nastavení představují strategická rozhodnutí pro zpracování vlny:

- Je-li šablona použita pro expedici položek pro prodejní objednávky a převodní příkazy nebo pro přesun položek do výroby pro výrobní zakázky nebo kanbany.
- Je-li vlna zpracována ručně nebo automaticky (viz následující):

  - **Ruční zpracování** – řádek je přidán do vlny a zásoby se rezervují, je však nutné vybrat **Zpracovat** na stránce se seznamem **Všechny vlny** a vytvořit práci výdeje pro danou objednávku.
  - **Automatické zpracování** – můžete úplně nebo částečně automatizovat zpracování vlny. Při plné automatizaci zpracování vlny je vytvořena vlna obsahující řádek z prodejní objednávky, výrobní zakázky nebo kanbanu při vytvoření prodejní objednávky, výrobní zakázky nebo kanbanu. Položky se odečtou od zásob na skladě a je vytvořena práce výdeje. Částečné zpracování vlny automatizaci umožňuje zadání hodnot, které spustí zpracování vlny. Například lze zadat maximální hmotnost dodávky, která spustí zpracování vlny, pokud dosáhne celková hmotnost řádků ve vlně určité hodnoty.

- Pokud přiřadíte dodávky k otevřené vlně. Například pokud slíbíte zákazníkům, že objednávka vystavená v 12:00 odp. bude expedována do 24 hodin, můžete vytvořit šablonu vlny a automaticky přiřadit řádky objednávky k otevřené vlně až do 12:00 odp. V tomto okamžiku dojde k automatickému zpracování vlny.

Při zpracování vlny se vytvoří výdej vycházející z šablony práce a směrnice skladového místa určené pro sklad. Šablona práce určuje, jak je výdej vytvořen, a směrnice skladového místa určují umístění pro výběr a vložení.

## <a name="create-a-wave-template"></a>Vytvoření šablony vlny

Chcete-li nastavit šablonu vlny, postupujte následujícím způsobem:

1. Přejděte do **Řízení skladu** \> **Nastavení** \> **Vlny** \> **Šablony vlny**.
1. Vyberte **Nová**, abyste mohli vytvořit novou šablonu vlny.
1. V poli **Typ šablony vlny** vyberte jednu z následujících možností:

    - *Expedice* – Použití šablony vlny pro dodávané položky z prodejní objednávky a převodních příkazů.
    - *Výrobní zakázky* – Použití šablony vlny pro přesunutí položek výrobní zakázky.
    - *Kanban* – Použití šablony vlny pro přesunutí položek kanbanové objednávky.

1. Do polí **Název šablony vlny** a **Popis šablony vlny** zadejte název a popis šablony vlny.

    > [!NOTE]
    > Pokud je pro sklad vytvořeno více šablon, bude číslo v poli **Pořadí šablony vlny** při splnění kritérií v šabloně určovat pořadí šablony v sekvenci, ve které jsou šablony použity. Volbami **Přesunout nahoru** nebo **Přesunout dolů** můžete změnit pořadí šablon.

1. V polích **Lokalita** a **Sklad** vyberte pracoviště a sklad, pro který šablona vlny vytvoří vlny a výdeje.
1. Pokud chcete automatizovat zpracování vlny, proveďte podle potřeby následující nastavení:

    - **Automatizovat vytvoření vlny**: Nastavte tuto možnost na *Ano*, chcete-li automaticky vytvořit vlnu při vydání prodejní objednávky, výrobní zakázky nebo kanbanu do skladu.
    - **Přiřadit k otevřeným vlnám** – Nastavením na *Ano* automaticky přiřadíte řádky k otevřené vlně, když jsou řádky uvolněny. Řádky jsou přiřazeny k vlně podle filtru dotazu pro šablonu vlny.
    - **Zpracovat vlnu při uvolnění do skladu** – Nastavením na *Ano* dojde k automatickému zpracování vlny a vytvoření práce, když je řádek uvolněn do skladu.
    - **Automaticky zpracovat vlnu při dosažení prahové hodnoty** – Nastavením na *Ano* dojde k automatickému zpracování vlny, pokud její hodnoty dosáhnou prahové hodnoty pro hmotnost, dodávku a řádky uvedené ve skupině polí **Prahové hodnoty vlny**. Toto nastavení je aktivní, pouze když je v poli **Typ šablony vlny** vybrána možnost *Expedice*.
    - **Automatizovat uvolnění vlny** – Nastavte na *Ano*, čímž se vlna automaticky uvolní. Výdej je vytvořen a je k dispozici pro mobilního zařízení.
    - **Automatizovat uvolnění práce doplnění** – Nastavením této možnosti na *Ano* můžete vytvořit práci doplnění podle poptávky a automaticky ji uvolnit. Do šablony vlny musíte přidat metodu doplnění vlny a vytvořit šablonu doplnění pomocí typu *Poptávka vlny*. Nastavte šablonu doplnění na stránce **Šablony doplnění**. To vyžaduje přidání metody doplnění do šablony vlny.
    - **Pokračovat ve zpracování vlny, pokud selže vytvoření práce** – Při nastavení na *Ano* systém použije prázdné umístění, pokud nemůže rezervovat zásoby v umístění navrženém směrnicí skladového místa (například protože zásoby již nejsou k dispozici). Při nastavení na *Ne* vlna selže, pokud systém nemůže rezervovat zásoby.

1. Nastavte skupinu polí **Prahové hodnoty vlny** podle potřeby:
    - **Prahová hodnota hmotnosti** – Zadejte maximální hmotnost, kterou může vlna obsahovat.
    - **Prahová hodnota dodávky** – Zadejte maximální počet dodávek, které lze zahrnout do vlny.
    - **Prahová hodnota řádku** – Zadejte maximální počet řádků, které lze zahrnout do vlny.

1. Ve skupině polí **Výchozí hodnoty** vyberte atributy vlny, které chcete použít jako další kritéria pro šablonu vlny. Atributy vlny jsou užitečné pro přiřazení dalších kritérií (například podle jména konkrétního odběratele) do šablony vlny. Na stránce **Atributy vlny** můžete vytvořit atributy. 

1. Nastavte **Zásady oznámení vlny** na zásady, které chcete použít pro generování oznámení souvisejících s vlnami, které používají tuto šablonu. Příklad zásady oznámení vlny najdete v části [Oznámení o provedení vlny](wave-execution-notifications.md).

1. Na pevné záložce **Metody** bude podokno **Vybrané metody** obsahovat metody pro vybraný typ šablony vlny. Metody vlny, které provádějí akce vytvořené šablonou, např. vytváření nebo rozdělení práce. Tyto akce jsou také označovány jako kroky vlny. Metody vlny jsou předdefinovány pro každý typ šablon vlny. Předdefinované metody vlny nelze odebrat, avšak můžete změnit pořadí metod a přidat další metody. Pokud například vytváříte šablonu vlny pro expedici, můžete přidat metody pro doplnění a vytváření kontejnerů. Vytváření kontejnerů ve vlně lze přidat do posloupnosti metod vlny a definovat tak vyváření kontejnerů pro řádky zpracované v šabloně vlny. Chcete-li přidat další metodu, postupujte následujícím způsobem:

    - V podokně **Zbývající metody** vyberte metodu a šipkou **Doleva** ji přidejte do podokna **Vybrané metody**.
    - Chcete-li změnit pořadí, vyberte metodu a vyberte šipku **Nahoru** nebo **Dolů**.

    > [!NOTE]
    > Při přidání metody se automaticky uvede v odpovídajícím umístění v pořadí kroků.

1. Chcete-li vytvořit dotaz, který bude párovat uvolněné řádky s příslušnou vlnou, vyberte **Upravit dotaz** v podokně akcí.
1. Pro ověření platnosti nastavení šablony vlny vyberte **Ověřit šablonu**.
