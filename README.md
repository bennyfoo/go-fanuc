# go-fanuc

go-fanuc is a Go library for working with FANUC robot data.

## Usage

Construct a new FANUC client, then use its methods to get data.

    import (
    	fanuc "github.com/onerobotics/go-fanuc"
    )

    c, err := fanuc.NewClient("127.0.0.1") // or fanuc.NewClient("./path/to/backup/dir")
    if err != nil {
    	return err
    }

    numregs, err := c.NumericRegisters()
    if err != nil {
    	return err
    }

    for _, r := range numregs {
    	fmt.Println(r)
    }
