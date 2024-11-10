# Deploying ML Models to Edge Devices

This is a tutorial on how to leverage several model compression techinques to store large models on smaller, more efficient devices. A full writeup will be availible once this project has concluded.

It might already be up so check https://01bbae.github.io/ if it is not linked already.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

The installation instructions for this tutorial will differ wildly depending on hardware and OS. Some pytorch modules for things like quantization will not work on MacOS metal, because the libraries are in beta and some are just not implemented.
I recommend running all of the model code to export the core ml package on Windows x86 instead. I provided an ```environment.yml``` file for conda installations, but this is just for reference as there are cuda packages that are also bundled and your hardware may not support it.

### Prerequisites

Recommended to run on Windows 11 x86 hardware 

Untested fully on MacOS (everything but quantization modules should work with minor tweaks to the code)


### Installing

Honestly, I can't give specific directions due to hardware, but using a virtual env  of your choice (pip or conda) install:

- python3.11.10
- pytorch2.5.1
- etc.

(See ```environment.yml``` for reference)

If you want to turn your models into coreml programs with executorch, you will also have to clone executorch from git. The links for the reference docs from pytorch are linked in the notebook under ```Quantizing and Exporting ... model``` section.

You can also install the accelerators of your choice (cuda, mps), but some of the code when exporting models will have to be done on CPU due to no code existing for accelerators.

## Deployment

This portion is a work in progress, but since the notebook exports the coreml model, you should be able to import it into a swift/xcode app for apple products.

## Built With

* [Pytorch](https://pytorch.org/) - The ML framework used
* [Core ML](https://developer.apple.com/documentation/coreml/) - Apple's ML framework library

## Contributing

I am currently not committed to taking pull requests but if you have any issues with the notebook or code, feel free to drop an issue for the repository.

## Authors

* **BJ Bae** -  [01bbae](https://github.com/01bbae)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* For the [README template](https://gist.github.com/PurpleBooth/109311bb0361f32d87a2#file-readme-template-md)
