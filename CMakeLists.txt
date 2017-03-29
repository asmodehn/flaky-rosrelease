cmake_minimum_required(VERSION 2.8.3)
project(flaky)

# Minimal Python module setup - catkin is assumed preinstalled along with ROS
# This assume catkin is installed along with a minimal ROS system.
find_package(catkin REQUIRED COMPONENTS
    catkin_pip
)

# defining current package as a package that should be managed by pip (not catkin - even though we make it usable with workspaces)
catkin_pip_package(flaky)

## Unit tests
if (CATKIN_ENABLE_TESTING)

    ############
    # NoseTests
    ############

    #catkin_add_nosetests(test/test_nose --with-flaky --exclude="test_nose_options_example")
    #catkin_add_pytests(test/test_pytest -k 'example and not options' --doctest-modules)
    #catkin_add_pytests(test/test_pytest -k 'example and not options' -n 1)
    #catkin_add_pytests(test/test_pytest/test_flaky_pytest_plugin.py -p no:flaky)
    #catkin_add_nosetests(test/test_nose/test_nose_options_example.py --with-flaky --force-flaky --max-runs 2)
    #catkin_add_pytests(test/test_pytest/test_pytest_options_example.py --force-flaky --max-runs 2)

    # TODO : use tox directly...

endif()
