---
title: Nastavení projektu pracovního příkazu
description: Toto téma vysvětluje nastavení projektu pracovního příkazu v modulu Správa majetku.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjectSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 19cdc33fcc9d1293b235facbaffd1ccf62875217
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6360046"
---
# <a name="work-order-project-setup"></a>Nastavení projektu pracovního příkazu

[!include [banner](../../includes/banner.md)]

 

V modulu **Správa majetku** je pro každou úlohu pracovního příkazu požadován vztah projektu. Projekt, který je přidružený k úloze pracovního příkazu, umožňuje sledovat náklady na různých projektech, které souvisejí se správou majetku, jako jsou například projekty interní údržby, projekty správy servisu a investiční projekty. 

## <a name="project-setup-for-a-work-order-job"></a>Nastavení projektu pro úlohu pracovního příkazu

Když na pracovním příkazu vytvoříte úlohu pracovního příkazu, nastavení projektu v modulu **Řízení projektů a účetnictví** a nastavení projektu pracovního příkazu v modulu **Správa majetku** určuje, jakým způsobem lze projekty použít pro řízení nákladů majetku vybraného na této úloze pracovního příkazu. V této části jsou popsány následující součásti nastavení projektu, které se používají pro pracovní příkaz: nadřazený projekt (ID projektu), typ projektu, projektové aktivity a finanční dimenze:

- Při vytváření úlohy pracovního příkazu na pracovním příkazu se automaticky vytvoří jedinečné ID projektu a související aktivita projektu. Obsahuje-li však několik úloh pracovního příkazu na pracovním příkazu stejný majetek, bude pro ně použito stejné ID projektu. Jinými slovy, ID jedno projektu je vytvořeno pro každý majetek na pracovním příkazu.

    - V nastavení nadřízeného projektu byl nalezen nadřazený projekt (ID projektu) pro úlohu pracovního příkazu. (Další informace o nastavení nadřazeného projektu naleznete v následujícím oddílu.) Pokud například přidružíte zákazníka nebo funkční místo k určitému nadřazenému projektu, bude nadřazený projekt použit při každém vytvoření pracovních příkazů pro daného odběratele nebo pro toto funkční umístění. Pokud nejste přihlášeni ke konkrétnímu ID projektu, například k funkčnímu místu, použije se další příslušný nadřazený projekt v nastavení projektu pracovního příkazu.
    - Typ projektu je požadován pro každé ID projektu. Typ projektu se nachází v nastavení skupiny projektů. (Další informace o nastavení skupiny projektů naleznete v následujícím oddílu.) Pokud v nastavení skupiny projektů nebude nalezena shodná položka, použije se nastavení skupiny projektů v nadřazeném projektu.
    - Nastavení pro vyžadování aktivit projektu v prognózách a denících se kopíruje z nadřazeného projektu do projektu pracovního příkazu. Pokud jsou možnosti **Hodiny**, **Výdaje** a **Položky** nastaveny na **Ano** pro projekt použitý jako nadřazený projekt, je pro prognózy a deníky povinná aktivita projektu. (Chcete-li získat přístup k těmto možnostem, vyberte **Řízení projektů a účetnictví** \> **Projekty** \> **Všechny projekty** a poté vyberte projekt, který se používá jako nadřazený projekt. Možnosti se nacházejí v části **Požadovat aktivitu v denících** na pevné záložce **Nastavení** .)

- Finanční dimenze se zkopírují z majetku a sloučí se s nadřazeným projektem.

Následující část vysvětluje, jak nastavit nadřazené projekty a skupiny projektů. Nadřazený projekt a nadřazené skupiny slouží k řízení pracovních příkazů. Rovněž se používají pro vytváření sestav o pracovních příkazech.

## <a name="set-up-work-order-projects"></a>Nastavení projektů pracovního příkazu

Než začnete vytvářet pracovní příkazy, je nutné nastavit projekty s pracovními příkazy. Stránka **Nastavení projektu pracovního příkazu** (**Správa majetku** \> **Nastavení** \> **Pracovní příkazy** \> **Nastavení projektu**) obsahuje dvě karty: **Nadřazený projekt** a **Skupina projektů**.

Na kartě **Nadřazený projekt** můžete nastavit vztahy projektu, které lze použít v případě, že pro majetek vybraný na pracovním příkazu není nastaven žádný projekt. Nastavení nadřazeného projektu není povinné, pokud vaše společnost používá majetkové projekty. Je relevantní pouze v případě, že chcete použít projekty s pracovním příkazem namísto majetkových projektů. V takovém případě je nutné nastavit alespoň jeden nadřazený projekt.

Na kartě **Skupina projektů** můžete nastavit skupiny projektů, které lze přidružit k typům pracovních příkazů, typům majetku a majetku.

Skupiny projektů lze použít k vytvoření specifických kategorií (skupin), které se používají pro řízení nákladů. Vytvoříte-li například skupiny projektů pro specifické typy majetku nebo typy pracovních příkazů, můžete provést podrobné sledování nákladů údržby podle typu.

Skupiny projektů nejsou povinné. Pokud nenastavíte skupiny projektů, použije se nadřazený projekt k určení skupiny projektů a podřízený projekt se vytvoří ze skupiny projektů nadřízeného projektu.

Nastavení umožňuje úplnou integraci s modulem **Řízení projektů a účetnictví**. Z tohoto důvodu lze sledovat náklady, které souvisejí s pracovními příkazy v souvisejících projektech. Následující postup popisuje nastavení pro projekty s pracovními příkazy.

1. Vyberte **Správa majetku** \> **Nastavení** \> **Pracovní příkazy** \> **Nastavení projektu**.
2. Na kartě **Nadřazený projekt** vyberte **Přidat**.
3. V polích **Typ pracovního příkazu**, **Funkční místo**, **Typ majetku** a **Majetek** vyberte hodnoty podle potřeby. Pro každý přidaný řádek lze nastavit pouze jedno nebo více polí. Počet polí, která jste nastavili, určuje kombinaci, která se použije při výběru ID projektu v modulu Správa majetku. 

    Pokud vyberete funkční místo, související podřízená umístění budou automaticky zahrnuta. Pokud vyberete majetek, můžete vytvořit více řádků nastavení projektu pro stejný majetek, ale pro daný majetek můžete vybrat různé projekty.

4. V poli **ID projektu** vyberte projekt, který se má vztahovat k nastavení, které jste vytvořili v kroku 3.
5. Pokud má nastavení projektu platit pouze pro omezené období, vyberte koncové datum v poli **Koncové datum**. V opačném případě vyberte **Žádný**.

    Ve výchozím nastavení je počátečním datem datum přidání projektu pracovní objednávky na stránku. Je ovládáno polem **Platné od**, které je ve výchozím nastavení skryto. Chcete-li zobrazit pole **Platné od**, vyberte **Zobrazit** \> **Vše**. Poté můžete použít pole **Platné od** spolu s polem **Koncové datum** pro nastavení omezené doby platnosti pro projekt pracovního příkazu.

    ![Stránka Nastavení projektu pracovních příkazů.](media/17-setup-for-work-orders.png)

6. Na kartě **Skupina projektů** vyberte **Přidat**.
7. V poli **Typ pracovního příkazu** vyberte typ pracovního příkazu.
8. Chcete-li, aby seskupení projektu bylo konkrétnější, vyberte typ majetku v poli **Typ majetku** nebo majetek v poli **Majetek**.
9. V poli **Skupina projektů** vyberte skupinu projektů, která by měla souviset s typem pracovního příkazu. Například typ pracovního příkazu s názvem **Preventivní údržba** může být přidružen ke skupině projektů s názvem **Předchozí údr.** nebo **Interní.** Alternativně, typ pracovního příkazu **Investice**, který se používá pro pracovní příkazy související s investicemi a s dlouhodobým majetkem, může být přidružen ke skupině projektů s názvem **Investovat** nebo **Investice**.
10. Zvolte možnost **Uložit**.

![Stránka nastavení projektu pracovních příkazů, přidání pracovního příkazu.](media/18-setup-for-work-orders.png)

> [!NOTE]
> Při každém vytvoření řádku pracovního příkazu vyhledá Správa majetku skupinu projektů, která by měla souviset s projektem pracovního příkazu. Hledání je založeno na nastavení popsaném v tomto tématu. Každá skupina projektů má související typ projektu. Skupiny projektů s **Časem a materiálem** nebo typem projektu **S pevnou cenou** jsou platné pouze pro majetek, který souvisí s účtem odběratele.
>
> U nadřazených projektů a skupin projektů je výběr založen na záznamech, které jste vytvořili pomocí předchozího postupu, když systém vybere dostupný projekt pracovního příkazu nebo skupinu projektů. Správa majetku prochází záznamy, které souvisejí s projektem pracovního příkazu, a slouží ke kontrole možného spárování. Vždy zkontroluje nejdříve nejkonkrétnější kombinaci. Jinými slovy, pro nadřazený projekt pracovního příkazu Správa majetku nejprve zkontroluje možnou shodu v poli **Majetek**. Pokud není nalezena shoda, zkontroluje shodu v poli **Typ majetku**. Pokud není nalezena shoda, zkontroluje shodu v poli **Funkční místo** a tak dále. Jak vidíte v rozvržení stránky **Nastavení projektu pracovního příkazu**, toto chování znamená, že pro nalezení nejspecifičtější kombinace zkontroluje Správa majetku každý záznam zprava doleva pro nalezení shody. Není-li nalezena žádná shoda, použije se výchozí záznam, v němž je vybrán pouze ID projektu. Proces vyhledání související skupiny projektů je podobný. Správa majetku nejprve zkontroluje možné párování pro pole **Majetek**, poté pole **Typ majetku** a poté pole **Typ pracovního příkazu**. Není-li nalezena žádná shoda, použije se výchozí záznam, v němž je vybrána pouze skupina projektu.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]