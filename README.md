# Alpyne

The **A**ny**L**ogic-**Py**thon con**ne**ctor

This is a Python library for interactively running models exported from the RL experiment. 

Currently, this library released as a **public beta** (so please excuse any rough edges). If you have problems or bugs, please file them in the `Issues` tab. For general talk or questions, there's the `Discussions` tab.

**UPDATE (Oct 2023):** An overhaul to the backend is currently an active WIP. Estimated release is EOY (likely sooner though).

Full documentation (with background information, getting started guide, and class docs) can be found @ https://t-wolfeadam.github.io/Alpyne

Installation
------------
Alpyne supports Python 3.6+

Install this library running the following command in a terminal prompt: ``pip install anylogic-alpyne``.

Preparing an AnyLogic model
---------------------------
You can use *any* edition of AnyLogic (PLE, University, or Professional) with this library. However, be aware that limitations of the edition will still apply. For example, PLE users executing models which utilize industry-specific libraries have their runs limited to 1-hour simulation time. 

You will need to setup your model with the following components.

1. RL experiment, with the Configuration, Observation, Action, and stopping conditions filled out, as per your specifications
2. A call to the RL experiment's ``takeAction`` method, at the moment you wish an action to be taken

To export the model, navigate to the properties of your RL experiment and click the option at the top to export it. If you do not see an option for Alpyne or generic 3rd parties, you may use the one for "Microsoft Bonsai".

Next Steps
----------
The API and overall workflow for Alpyne is intentionally similar to the AnyLogic Cloud. In your Python code, you will create a single Client object, passing a reference to where your exported model is located, in addition to setting other options. This object then gives you access to templates for the inputs/outputs of the model in addition to methods for creating new model runs, which can then be interacted with.

For more, see the [documentation page](https://t-wolfeadam.github.io/Alpyne), download the provided examples, or post in the Discussions tab.
