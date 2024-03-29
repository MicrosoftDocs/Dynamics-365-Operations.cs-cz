---
title: Vytvoření seznamů úkolů a přidání úkolů
description: Tento článek popisuje, jak vytvořit seznamy úkolů a jak do nich přidat úkoly v řešení Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: b81f27f79362516f8a25766c1f663a7691ebb42a
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746152"
---
# <a name="create-task-lists-and-add-tasks"></a>Vytvoření seznamů úkolů a přidání úkolů

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak vytvořit seznamy úkolů a jak do nich přidat úkoly v řešení Microsoft Dynamics 365 Commerce.

*Úkol* definuje určitou část práce nebo akci, kterou musí dokončit v určitém termínu splnění nebo před ním. V Dynamics 365 Commerce může úkol obsahovat podrobné pokyny a informace o kontaktní osobě. Může rovněž zahrnovat odkazy na operace administrativy, operace pokladního místa (POS) nebo stránky webu, aby se zvýšila produktivita a byl poskytnut kontext, který vlastník úkolu potřebuje k efektivnímu dokončení úkolu.

*Seznam úkolů* je sada úkolů, které je nutné provést jako součást obchodního procesu. Může se například jednat o seznam úkolů, které musí nový pracovník provést během náboru, seznam úkolů pro pokladníky na noční směně nebo seznam úkolů, které musí být provedeny v rámci přípravy obchodu na nadcházející letní sezónu. V Commerce lze každý seznam úkolů s cílovým datem přiřadit libovolnému počtu obchodů nebo zaměstnanců a lze u něj nastavit opakování.

Seznamy úkolů mohou v administrativě Commerce vytvářet manažeři i pracovníci a poté je přiřadit k sadě obchodů.

## <a name="create-a-task-list"></a>Vytvoření seznamu úkolů

Před zahájením procesu vytváření seznamu úkolů se ujistěte, že jste dokončili konfigurace v článku [Nakonfigurujte správu úloh](task-mgmt-configure.md). Pokud chcete vytvořit seznam úkolů, postupujte následovně.

1. Přejděte na **Retail a Commerce \> Správa úkolů \> Řízení správy úkolů**.
1. Vyberte možnost **Nový** a poté zadejte hodnoty do polí **Název**, **Popis** a **Vlastník**.
1. Zvolte **Uložit**.

## <a name="add-tasks-to-a-task-list"></a>Přidání úkolů do seznamu úkolů

Chcete-li přidat úkol do seznamu úkolů, postupujte takto.
 
1. Na pevné záložce **Úkoly** v existujícím seznamu úkolů přidejte úkol výběrem možnosti **Nový**.
1. V dialogovém okně **Vytvořit nový úkol** zadejte v poli **Název** jedinečný název úkolu.
1. Do pole **Posun termínu splnění od cílového data** zadejte kladnou nebo zápornou celočíselnou hodnotu. Zadáte například hodnotu **-2** v případě, že má být úkol dokončen dva dny před termínem splnění seznamu úkolů.
1. Do pole **Poznámky** zadejte podrobné pokyny.
1. V poli **Kontaktní osoba** zadejte název odborníka na danou problematiku, kterého může vlastník úkolu kontaktovat v případě, že potřebuje pomoc.
1. V poli **Odkaz na úkol** zadejte odkaz na základě povahy úkolu.

> [!TIP]
> Ačkoli můžete při vytváření seznamu úkolů použít pole **Přiřazeno k** pro přiřazení úkolů některému uživateli, doporučujeme vyhnout se přiřazování úkolů při vytváření seznamu úkolů. Namísto toho přiřaďte úkoly po vytvoření instance seznamu pro jednotlivé obchody.

## <a name="use-task-links-to-help-improve-worker-productivity"></a>Použití odkazů na úkoly pro zvýšení produktivity pracovníků

Commerce vám umožňuje propojit úkoly s konkrétními operacemi POS, jako je například spuštění sestavy prodeje, zobrazení školicího videa online pro orientaci nového zaměstnance nebo provedení operace administrativy. Tato funkce pomáhá vlastníkům úkolů získat informace, které potřebují k efektivnímu dokončení úkolu.

Chcete-li při vytváření úlohy přidat odkazy na úkoly, postupujte podle následujících kroků.

1. Na pevné záložce **Úkoly** v existujícím seznamu úkolů vyberte možnost **Upravit**.
1. V dialogovém okně **Upravit úkol** v poli **Odkaz na úkol** vyberte jednu nebo více z následujících možností:

    - Vyberte **položku nabídky**, pro kterou chcete konfigurovat operaci zálohování, například „Produktové sady“.
    - Vyberte **Operace POS**, chcete-li konfigurovat operaci POS, například „Prodejní sestavy“.
    - Vyberte možnost **Adresa URL** pro konfiguraci absolutní adresy URL.

Na následujícím obrázku je znázorněn výběr propojení úkolů v dialogovém okně **Upravit úkol**.

![Výběr odkazů na úkoly v dialogovém okně Upravit úkol.](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a>Konfigurace operace POS, aby ji bylo možné propojit s úkolem

Chcete-li nakonfigurovat operaci POS, aby ji bylo možné propojit s úkolem, postupujte následovně.

1. Přejděte do nabídky **Retail a Commerce \> Instalace kanálu \> Nastavení POS \> POS \> Operace POS**.
1. Vyberte možnost **Upravit**, vyhledejte operaci POS a zaškrtněte u ní políčko **Povolit správu úkolů**.

## <a name="additional-resources"></a>Další zdroje

[Přehled správy úkolů](task-mgmt-overview.md)

[Konfigurace správy úkolů](task-mgmt-configure.md)

[Přiřazení seznamů úkolů k obchodům nebo zaměstnancům](task-mgmt-assign-lists.md)

[Správa úkolů v POS](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
