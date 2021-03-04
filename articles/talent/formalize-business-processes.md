---
title: Formalizace obchodních procesů
description: Toto téma vysvětluje, jak můžete použít funkci obchodního procesu k vytvoření šablony obchodního procesu pro procesy, které je třeba dokončit v rámci vaší organizace.
author: andreabichsel
manager: AnnBe
ms.date: 01/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: PersonnelBusinessProcessGenericWorkspace, BusinessProcessGenericTemplateListpage, BusinessProcessGenericMyTemplates, BusinessProcessGroupAssignment
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-01-09
ms.dyn365.ops.version: AX 7.1.0, Talent October 2017 update
ms.openlocfilehash: 0f4d2b8e5f78c5815c5ad7e5eae0d13ad7d15c12
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460523"
---
# <a name="formalize-business-processes"></a>Formalizace obchodních procesů

Funkce Obchodní proces vám umožňuje vytvořit šablonu obchodního procesu pro obchodní procesy, které je třeba dokončit v rámci vaší organizace. Vaše společnost například ukončuje audit lidských zdrojů každý rok. V takovém případě můžete vytvořit šablonu, která sleduje všechny úlohy, ze kterých se skládá proces auditu. Tato šablona pak může pomoci zajistit, aby všechny úlohy byly prováděny pokaždé, když se uskutečňuje audit. Dále pokud musí být úkoly dokončeny v určitém pořadí, šablona může pomoci zajistit, aby se provedly ve správném pořadí.

Šablony lze znovu použít pro opakující se procesy. Mohou být také zkopírovány a používány jako výchozí bod pro vytvoření nových šablon.

Po vytvoření šablony obchodního procesu lze obchodní proces spustit a sledovat v pracovním prostoru **Obchodní proces**. Při spuštění obchodního procesu jsou přiřazeny úlohy odpovídajícím osobám a obsahují data splnění.

## <a name="business-process-templates"></a>Šablony obchodního procesu
Šablona obchodního procesu uvádí skupinu úkolů, které tvoří obchodní proces. Obchodní procesy ve výchozím nastavení mohou vytvářet správci lidských zdrojů a asistenti ve výchozím nastavení. Můžete však změnit role, které mohou vytvořit obchodní procesy úpravou funkčního oprávnění **Udržovat obecné obchodní procesy** v konfiguraci zabezpečení.

Vlastníka procesu lze definovat pro každý obchodní proces. Vlastník procesu má přehled o všech úlohách procesu a může opětovně přiřadit úkoly nebo změnit datum splnění. Ředitel lidských zdrojů například vytvoří šablonu obchodního procesu pro revizi zaměstnaneckých výhod a určí manažera kompenzací a zaměstnaneckých výhod jako vlastníka procesu. Manažer kompenzací a zaměstnaneckých výhod má poté viditelnost do úkolů, které je třeba dokončit jako součást kontroly.

Vlastník procesu nemůže vytvořit nové obchodní procesy nebo šablony obchodních procesů, nebo odstranit aktivní obchodní procesy nebo šablony obchodních procesů.

## <a name="tasks"></a>Úlohy
Obchodní proces se často sklád z více úkolů. Některé úlohy, jako je například kontrola nabídek interních kurzů, lze dokončit v rámci aplikace Microsoft Dynamics 365 Talent. V tomto případě je možnost zvolena v poli **Odkaz na úkol**. Ostatní úlohy mohou zahrnovat revize nebo vyplňování stránek na webové stránce. V tomto případě je zvoleno **URL** v poli **Odkaz na úkol** a poté lze zadat webovou adresu. Pro externí a interní weby můžete zadat adresy URL. Můžete také vytvořit úkoly pro aktivity, které provádíte ručně, například kontrolu přístupu všech struktur. V takovém případě není požadován odkaz na úkol. Tato flexibilita vám umožňuje sledovat více druhů úloh v komplexním procesu.

Úlohy lze přiřadit buď ke konkrétnímu pracovníkovi nebo pozici. Například manažer kompenzací a zaměstnaneckých výhod bude vždy osoba, která provádí kontrolu náhrad pojistného. Proto když vytvoříte tuto úlohu, vyberte **Pozice** v poli **Typ přiřazení** a poté zvolte **Manažer kompenzací a zaměstnaneckých výhod** v seznamu **Pozice**. Po spuštění obhodního procesu se přiřadí úloha k pracovníkovi, který je na pozici **Manažer kompenzací a zaměstnaneckých výhod**. Chcete-li přiřadit úkol konkrétnímu pracovníkovi, zvolte **Pracovník** v poli **Typ přiřazení** a poté vyberte příslušnou osobu.

Data splnění úkolů závisí na cílovém datu zadaném na začátku obchodního procesu. Některé úlohy musí být dokončeny před cílovým datem a jiné úlohy mohou být dokončeny po cílovém datu. Při definování úkolu zadáte v poli **Posun data splatnosti od cílového data** datum splnění, které je relativní k cílovému datu. Například manažer kompenzací a zaměstnaneckých výhod musí provést kontrolu náhrad pojistného do 10 dní před dokončením auditu lidských zdrojů. V takovém případě úkol vytvořený pro kontrolu má hodnotu **Posun data splatnosti od cílového data** **-10**. Je-li obchodní proces zahájen 13. května, úloha má datum splnění 3. května.

> [!NOTE]
> Data splatnosti lze upravit také po zahájení obchodního procesu.

Komplexní úkoly mohou vyžadovat více kroků, nebo osoby provádějící úlohy musí poskytnout další informace. Pro tyto situace lze přidat instrukce k úkolu. Pokyny mohou poskytovat osobě přiřazené k dokončení úlohy další informace o tom, jak úlohu dokončit. Do pokynů můžete dokonce zahrnout formátování RTF.

## <a name="starting-a-business-process"></a>Spuštění obchodního procesu
V šabloně obchodního procesu můžete spustit obchodní proces volbou **Spustit proces**. Při zahájení procesu jsou vytvořeny úlohy pro vybrané pracovníky anebo pozice, definované v úlohách, které jsou zahrnuty v šabloně. Každému úkolu bude také přiděleno datum splatnosti přidáním nebo odebráním počtu dnů posunu od cílového data, jak je vysvětleno v části Úlohy. Aktivní obchodní procesy lze zobrazit v pracovním prostoru **Obchodní procesy**.

## <a name="employee-self-service"></a>Samoobsluha pro zaměstnance
Po přiřazení úlohy zaměstnanci si ji může zaměstnanec zobrazit a všechny další přiřazené úlohy na stránce **Samoobsluha pro zaměstnance**. Pro každý úlohu obchodního procesu přiřazené zaměstnanci může tento zaměstnanec zobrazit jméno a popis úlohy, pokyny pro dokončení a jméno kontaktní osoby. Ze stránky **Samoobsluha pro zaměstnance** mohou zaměstnanci také otevřít přidruženou stránku aplikace Microsoft Dynamics 365 nebo přidruženou webovou stránku, a mohou označit probíhající, zrušené nebo dokončené úlohy.

## <a name="business-process-workspace"></a>Pracovní prostor obchodního procesu
Odborníci na personalistiku mohou zobrazovat aktivní obchodní procesy v pracovním prostoru **Obchodní proces**. Tento pracovní prostor uvádí seznam všech aktivních procesů a úloh, které jsou přidružené ke každé úloze. Komplexní seznam úloh lze filtrovat podle data splatnosti. Pracovní prostor zobrazuje také úlohy po termínu a úkoly konkrétně přiřazené odborníkovi lidských zdrojů. Odborník lidských zdrojů může též aktualizovat stav všech úloh a v případě potřeby opětovně přiřadit úlohy pro udržení postupu celkového obchodního procesu.

## <a name="my-business-processes-workspace"></a>Pracovní prostor Moje obchodní procesy
Vlastníci procesu mohou zobrazit aktivní obchodní procesy, které jim jsou přiřazeny v pracovním prostoru **Můj obchodní proces**. Tento pracovní prostor uvádí seznam všech aktivních procesů, které tento uživatel vlastní, a přidružených úloh. Komplexní seznam úloh lze filtrovat podle data splatnosti. Pracovní prostor zobrazuje také úlohy konkrétně přiřazené vlastníkovi procesu. Vlastník procesu může také aktualizovat stav všech úloh a opětovně přiřadit jakoukoliv úlohu.

## <a name="navigating-business-processes"></a>Procházení obchodních procesů
Chcete-li vytvořit nebo kopírovat šablonu obchodního procesu, nebo spustot obchodní proces, přejděte na Obchodní procesy - odkazy – Správa obchodních procesů. Poté můžete provést následující akce:

- Vyberte **Nová** pro vytvoření nové šablony obchodních procesů.
- Zvolte **Kopírovat ze šablony**, chcete-li kopírovat vybranou šablonu do nové.
- Zvolte **Spustit proces** pro spuštění vybraného obchodního procesu, přiřadění úlohy a vypočítání data splatnosti.

Chcete-li zobrazit aktivní procesy a přidružené úlohy, otevřete pracovní prostor **Obchodní procesy**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]